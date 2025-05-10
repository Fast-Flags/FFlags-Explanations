# Move Prerender
```json
{
  "FFlagMovePrerender": "True",
  "FFlagMovePrerenderV2": "True"
}
````

**What It Does:**
This flag moves the `prerender` task to run *after* everything else is completed on the off thread. By default, `prerender` runs first, which causes the render thread to wait until `prerender` finishes before it can start rendering a frame.

With this flag enabled, `prerender` is executed while the main thread is still processing the previous frame. This means the main thread doesn't need to wait for `prerender` to complete as often, improving framerates — at the cost of slightly increased frame latency.

**My Results:**
Enabling this flag increased my framerate from **80 FPS to 100 FPS** in **Pls Donate** at **Graphics Level 10 (FRM 21)**, 1080p, using an **R5 7600X / RX 7600** setup.

**Notes:**

* This flag benefits CPU-bound scenarios the most.
* It *may* cause issues in some games, though I haven’t encountered any yet.
* Games I’ve tested without problems:

  * Pls Donate
  * Neighbors
  * On Tap 17+
  * Pinewood Computer Core

# Move Prerender V2
This flag has been forced to **True**, meaning it will be enabled for everyone.
It's an additional optimization to the original `Move Prerender`.

```json
{
  "FFlagMovePrerenderV2": "True"
}
```

**Screenshots:**
Below are before-and-after comparisons taken from the microprofiler.

![Image](https://media.discordapp.net/attachments/1285949000595275847/1370822948063019139/Screenshot_2024-10-27_135857_1.png?ex=6820e5db&is=681f945b&hm=a4fe1ba33933ab7ef07122c217dcfea17942569900e56ebf33c41c96a70f8b0e&=&width=1344&height=833)
![Image](https://media.discordapp.net/attachments/1285949000595275847/1370822947681599689/Screenshot_2024-10-27_135857_2.png?ex=6820e5db&is=681f945b&hm=0f602c0295ef5f1ec8ee697ddf800ea522dd3ea4a74eeca7a1ea5f3949eb08e6&=&width=1344&height=833)
