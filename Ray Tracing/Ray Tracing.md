# Ray Tracing

## Shadow Mapping

Using rasterization to show shadows

It's an image-space algorithm, and we have no knowledge of scene's geometry during shadow computation and we must deal with aliasing aritifacts

**Key Idea**: the points **not** in shadow must be seen both **by the light** and **by the camera**

**Pass 1** : Render from Light

Getting depth image from light source, record the depth ofpoint that can be seen

**Pass 2** : Project to Light

Project visible points in eye view back to light source

If the depth of the point gotten by the are equals to the depth gotten by the light source, the point is not in the shadow

Shadow maps can only create hard shadows

![Carol](H&S.png)

Soft shadow arises from that the light source has its size, so that in some points you can only see part of the light

![Carol](Soft_Shadow.png)