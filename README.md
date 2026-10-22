# Autonomous Multi-Robot System for Warehouse Operations

A centralized-planning, decentralized-control framework for a fleet of identical warehouse robots. Tasks arrive at random. Small items go to a single robot, and large items get a team of robots that carries them together in formation. Modeled and simulated in MATLAB.

## Three control layers

1. **Task allocation:** a greedy iterative auction assigns incoming tasks to robots, minimizing idle time and travel cost, and keeps re-planning as tasks keep arriving.
2. **Cooperative transport:** a decentralized leader-follower formation controller, with asymptotic stability proved by Lyapunov's direct method (formation error → 0).
3. **Collision avoidance:** an artificial potential field with a "partner-aware" filter, so robots repel everything except their own formation partners.

## Results

- Formation error converged to zero over continuous runs (T > 60 s)
- Collision-free with 10 robots in a 14 m × 10 m workspace
- Robots switched between idle, solo task and team task without stopping

Full math, proofs and simulation results are in the [report](docs/Project_Report.pdf).

## Team

Nitin Kothakonda, Chakradhar Reddy Lakkireddy, Krishna Vamshi Challa. MAE 598 Multi-Robot Systems, Arizona State University, Fall 2025.
