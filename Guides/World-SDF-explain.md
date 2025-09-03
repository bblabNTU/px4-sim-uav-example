# Gazebo World SDF explain

## Physics

```xml

<physics type="ode">
  <max_step_size>0.004</max_step_size>
  <real_time_factor>1.0</real_time_factor>
  <real_time_update_rate>250</real_time_update_rate>
</physics>
```

- type="ode": Specifies the physics engine as ODE (Open Dynamics Engine).
- max_step_size: The time step size in seconds for each simulation iteration. Lower values can increase accuracy.
- real_time_factor: The ratio of simulation time to real-world time.
- real_time_update_rate: The maximum number of iterations per second.

## Plugins

Plugins enhance the functionality of the simulation, such as physics calculations, sensor models, etc.

```xml

<plugin name='gz::sim::systems::Physics' filename='gz-sim-physics-system'/>
```
- name: A unique name for the plugin.
- filename: The library where the plugin code is located.

## GUI

This sets up the graphical interface elements. Various GUI plugins like 3D View, World Control, and World Stats are configured here.
Environment

```xml

<gravity>0 0 -9.8</gravity>
<magnetic_field>6e-06 2.3e-05 -4.2e-05</magnetic_field>
<atmosphere type='adiabatic'/>
```
- gravity: Specifies the gravity vector in x, y, z coordinates.
- magnetic_field: Specifies the magnetic field vector.
- atmosphere: Defines the atmospheric model. "Adiabatic" is one of the options.

## Scene

```xml
<scene>
  <grid>false</grid>
  <ambient>0.4 0.4 0.4 1</ambient>
  <background>0.7 0.7 0.7 1</background>
  <shadows>true</shadows>
</scene>
```
- grid: Whether to show the grid.
- ambient: The ambient light color.
- background: The background color of the rendering window.
- shadows: Enable/Disable shadows in the rendering.
