Read the attached text and answer the following:

1. **State of an object**: The state of an object in a physics engine is typically defined by its position, velocity, and acceleration at a given time.
    
2. **Time step**: A time step is a small interval of time used in the simulation. It represents the amount of time that passes in the system for each iteration or step of the simulation.
    
3. **Acceleration of a body**: The acceleration of a body is calculated by summing up all the forces applied to it (gravity, friction, etc.), and then dividing by the mass of the body. This is based on Newton’s second law of motion.
    
4. **Advantage of Symplectic Euler Integration over Explicit Euler Integration**: Symplectic Euler Integration is more stable than Explicit Euler Integration for certain types of problems, especially those involving oscillatory motion. This is because it conserves energy over long periods of time, which is not the case with Explicit Euler Integration.
    
5. **Velocity calculation in Verlet’s integration**: In Verlet’s integration, the velocity is not explicitly calculated. Instead, the new position is calculated based on the previous position and the acceleration during the time step. However, if needed, the velocity can be estimated by subtracting the previous position from the current position and dividing by the time step.
