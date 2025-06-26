# 💣 MOP Bomb Impact Simulation

A realistic 3D simulation of a GBU-57 Massive Ordnance Penetrator (MOP) impacting a custom-sized target building, built with [Three.js](https://threejs.org/). Users can dynamically configure the building's dimensions and bomb weight to observe scaled, physics-informed destruction results in real time.


<img width="1776" alt="Screenshot 2025-06-26 at 10 56 25 AM" src="https://github.com/user-attachments/assets/f0deb7d8-5873-4ecf-9f98-9e002e6f4722" />


---

## 🚀 Features

- 🌇 **Real-time 3D Graphics**: Rendered using WebGL + Three.js
- 🏢 **Customizable Building**:
  - Set building **height**, **width**, and **thickness**
  - Building is constructed layer-by-layer and partially destructible
- 💥 **Dynamic Bombing Simulation**:
  - Set bomb **weight in pounds**
  - Impact destroys a proportion of the building based on physics-based damage ratio
- ☀️ **Realistic Environment**:
  - Daylight sky
  - Ground plane with texture
  - Lighting and fog for depth
- 🧱 **Destruction Physics**:
  - Partial destruction
  - Debris fragments fly outward based on impact strength
- ⚙️ **Real-Time UI Control**:
  - Input fields update building dimensions instantly without reloading
  - Manual trigger to drop bomb

---

## 📊 Physics Model

```text
volume = width * height * depth
damageRatio = weight / (volume / 2)
destroyCount = damageRatio * number of building layers

