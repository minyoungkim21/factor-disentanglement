# Factor Disentanglement

## (Supervised) Regression between x (image) and z (5-dim true factors, each [-1,+1]-scaled/normalized)


### Setup (brief)
- The same encoder model for x -> z regression
- The same decoder model for z -> x regression


### Latent traversal

[ x | z1 | z2 | z3 | z4 | z5 ]

![fixed_ellipse](https://user-images.githubusercontent.com/44901665/48269786-6a59b200-e406-11e8-9d45-33e3d725e2dd.gif) <br />
![fixed_heart](https://user-images.githubusercontent.com/44901665/48269792-6cbc0c00-e406-11e8-824b-74c07c7eda7b.gif) <br />
![fixed_square](https://user-images.githubusercontent.com/44901665/48269795-6f1e6600-e406-11e8-9ff6-e6db5b9eb256.gif) <br />
![random_img](https://user-images.githubusercontent.com/44901665/48269797-70e82980-e406-11e8-8477-920e8caf136e.gif) <br />


### Losses and Metrics (At iter# = 108K)

loss_z: 0.278   (\sum_j ||z_j - z*_j|, note: zj \in [-1,+1])  <br />
loss_x: 15.478  (\sum_i CE(x_i; x*_i); note: dim(x) = 64*64 = 4096)

metric1 = 0.9950  <br />
metric2 = 0.9850
