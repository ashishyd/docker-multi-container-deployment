To create frontend production image
`docker build -f frontend/Dockerfile.prod -t ashishyd/goals-react ./frontend`

The problem running both backend and frontend in same ECS cluster would be both are exposed to port 80.
There is no way 2 containers can run on same port.

To overcome this we create different task for frontend and backend, that is the reason we have to create backendUrl variable.

For production, use AWS LB url should be used as it will not change