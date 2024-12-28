# Mathematics for Two-Wheeled Differential Drive Robot

![Robot Movement](robot%20movement.png)

Given:

- $d_1$ is the distance traveled by the right wheel
- $d_2$ is the distance traveled by the left wheel
- $K$ is a constant
- $L$ is the distance between wheels
- $C$ is the distance from the center of rotation to the center of the robot
- $\alpha$ is the angle of rotation

$K = \frac{2 \cdot \pi}{360}$

## Distance traveled by the wheels

$d_1 = \alpha \cdot K \cdot (C + \frac{L}{2})$

$d_2 = \alpha \cdot K \cdot (C - \frac{L}{2})$

Two equations with two unknowns. $\alpha$ and $C$ can be calculated from the equations.

## Angle of the robot

$\alpha = \frac{d_1}{K \cdot (C + \frac{L}{2})}$

## Center of rotation of the robot

$d_2 = \frac{d_1}{K \cdot (C + \frac{L}{2})} \cdot K \cdot (C - \frac{L}{2})$

$d_2 = \frac{d_1}{C + \frac{L}{2}} \cdot (C - \frac{L}{2})$

$d_2 \cdot (C + \frac{L}{2}) = d_1 \cdot (C - \frac{L}{2})$

$d_2 \cdot C + \frac{d_2 \cdot L}{2} = d_1 \cdot C - \frac{d_1 \cdot L}{2}$

$C*(d_1 - d_2) = \frac{L}{2} * (d_1 + d_2)$

$C = \frac{L}{2} * \frac{d_1 + d_2}{d_1 - d_2}$

## Angle of the robot with respect to the center of rotation

$\alpha = \frac{d_1}{K \cdot (C + \frac{L}{2})}$

$\alpha = \frac{d_1}{K \cdot (\frac{L}{2} * \frac{d_1 + d_2}{d_1 - d_2} + \frac{L}{2})}$

$\alpha = \frac{d_1}{K \cdot \frac{L}{2} * (\frac{d_1 + d_2}{d_1 - d_2} + 1)}$

$\alpha = \frac{d_1}{K \cdot \frac{L}{2} * \frac{d_1 + d_2 + d_1 - d_2}{d_1 - d_2}}$

$\alpha = \frac{d_1}{K \cdot \frac{L}{2} * \frac{2d_1}{d_1 - d_2}}$

$\alpha = \frac{d_1}{K \cdot L * \frac{d_1}{d_1 - d_2}}$

$\alpha = \frac{d_1}{K \cdot L} \cdot \frac{d_1 - d_2}{d_1}$

$\alpha = \frac{d_1 - d_2}{K \cdot L}$

## X and Y coordinates of the robot

$x = C \cdot \cos(\alpha)$

$y = C \cdot \sin(\alpha)$
