# Lorenz Attractor

The Lorenz attractor is a well-known example of a chaotic system that exhibits complex, non-linear behavior. It was discovered by Edward Lorenz in 1963 while studying atmospheric convection. The attractor is defined by a set of three coupled differential equations, and its visualization provides fascinating insights into chaotic dynamics.

![Lorenz Attractor](https://github.com/victormeloasm/LorenzAttractor/blob/main/Example.jpg)

## How it Works

The Lorenz attractor is governed by the following system of differential equations:

```
dx/dt = sigma * (y - x)
dy/dt = x * (rho - z) - y
dz/dt = x * y - beta * z
```

where `x`, `y`, and `z` represent the state variables, and `sigma`, `rho`, and `beta` are parameters that control the behavior of the system.

To generate the Lorenz attractor, the differential equations are numerically solved using an ODE solver, such as the `ode45` function in MATLAB. The solver computes the trajectories of the state variables over a specified time interval.

## Usage

To generate and visualize the Lorenz attractor, follow these steps:

1. Install MATLAB (if not already installed) and ensure it is properly configured on your system.

2. Clone or download the repository containing the Lorenz attractor code.

3. Open MATLAB and navigate to the directory where the code files are located.

4. Modify the parameters `rho`, `sigma`, `beta`, `initV`, and `T` in the `lorenz.m` file to adjust the behavior and visualization of the attractor. The default values provide a good starting point.

5. Run the `lorenz.m` script in MATLAB. This will generate the trajectories of the state variables and display a 3D plot of the Lorenz attractor.

6. Explore the generated plot by rotating, zooming, and examining the intricate structure of the attractor.

## Example

Here's an example usage of the Lorenz attractor code:

```matlab
rho = 28;
sigma = 10;
beta = 8/3;
initV = [0 1 1.05];
T = [0 25];
eps = 0.000001;

[x, y, z] = lorenz(rho, sigma, beta, initV, T, eps);

figure;
plot3(x, y, z, 'color', [0 0.5 0], 'LineWidth', 2);
axis tight;
grid on;
xlabel('X');
ylabel('Y');
zlabel('Z');
title('Lorenz attractor');
```

This example generates a Lorenz attractor using the specified parameter values and displays a 3D plot with green lines.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
