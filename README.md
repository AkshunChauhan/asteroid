# Asteroid Visualizer: Planetary Defense & Impact Simulator

**NASA Space App Challenge Edmonton - First Prize Recipient**

---

## Project Overview

The Asteroid Visualizer is a sophisticated, interactive 3D platform developed to analyze and simulate the consequences of asteroid impacts on Earth. Designed for the NASA Space App Challenge, this tool serves as a technical demonstration of planetary defense assessment, leveraging real-time geospatial data and physical modeling to estimate the impact of Near-Earth Objects (NEOs).

The application allows researchers and policy makers to simulate impact scenarios with precise control over projectile parameters, geography, and mitigation strategies, providing immediate visual and quantitative feedback.

## Key Technical Features

### Advanced 3D Earth Visualization
Leverages `react-globe.gl` and `Three.js` for high-performance rendering of the terrestrial sphere, supporting interactive camera controls and precise mapping of geospatial coordinates.

### Impact Physics & Simulation
Features a robust simulation engine capable of modeling various asteroid strike scenarios:
- **Parameter Control:** User-defined inputs for diameter (meters), velocity (km/s), and impact angle (degrees).
- **Execution Environments:** Support for Ground, Airburst, and Water impact models, adjusting the physical footprint based on burst altitude and surface medium.

### Geospatial Analytics
- **Dynamic Zoning:** Real-time calculation and visualization of Severe, Major, and Light impact radii.
- **Population Impact Assessment:** Integration of randomized kernel density estimation to provide data-driven estimates of affected populations and potential casualties.
- **Topographical Labels:** Conditional rendering of major urban centers within proximity to the strike zone.

### Mitigation Strategy Sandbox
A testing environment for planetary defense protocols:
- **Kinetic Deflection:** Modeling the efficacy of Δv changes factored against various lead times.
- **Civilian Evacuation:** Radius-based evacuation modeling with configurable coverage metrics.

### Automated Reporting
- **AI-Driven Assessment:** Integration with Large Language Models (LLMs) to synthesize site-specific mitigation recommendations.
- **PDF Export:** Generation of formal, technical reports including impact KPIs, damage distribution charts, and strategic advice.

## Technical Architecture

### Core Stack
- **Frontend Framework:** React 19 (Vite)
- **Visualization:** Three.js, React Three Fiber, react-globe.gl
- **Geospatial Processing:** Deck.gl, GeoJSON integration
- **State Management:** Jotai (Atomic state architecture)
- **Data Visualization:** Recharts
- **Document Generation:** jsPDF
- **Backend Services:** Node.js / Express.js

## Scientific Framework

The simulation adopts established physical models for impact energy calculation:
1. **Kinetic Energy:** $E_k = \frac{1}{2}mv^2$, driving the primary damage scaling.
2. **Scaling Laws:** Radii calculations are derived from projectile volume and velocity, adjusted for impact angle and atmospheric interaction.
3. **Atmospheric Interaction:** Factors in Airburst scenarios where altitude significantly affects shockwave propagation and thermal radiation reach compared to ground strikes.

## Setup and Installation

### Prerequisites
- Node.js (Version 18 or higher)
- npm or yarn package manager

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AkshunChauhan/asteroid.git
   cd asteroid-visualizer
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure Environment Variables:
   Create a `.env` file in the root directory and provide the necessary API keys:
   ```env
   REACT_APP_OPENAI_API_KEY=your_production_key
   ```

4. Launch Development Server:
   ```bash
   npm run start
   ```

---
*Developed for the NASA Space App Challenge Edmonton.*
