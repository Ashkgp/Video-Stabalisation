##Video Stabilisation

Detects the previous image positions and predicts the next frame using kalman filter and Gaussian curve.

Any sharp change from the prediction is neutralised and is mean gaussian is taken to smoothen then flow.

Different values of cstd and pstd can influence the prediction and trajectory of the image thus resulting in greater or less stabilisation accordingly.

Stabilisation results in loss of pixels from the edge and thus the final image needs to be cropped out to remove the blank pixels from the sides of the image.

It's value can be changed by changing the value of macros 
```sh
HORIZONTAL_BORDER_CROP = 20
SMOOTHING_RADIUS = 5

```
