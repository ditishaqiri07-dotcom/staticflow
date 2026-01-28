# Coolify note (school VPN limitation)

Goal: deploy the same static site container to Coolify (self-hosted).

Issue: On the university WireGuard VPN, Docker networking / inbound access required for a Coolify setup can be restricted.
Because of this, a reliable Coolify deployment could not be guaranteed in the university network environment.

Self-hosted equivalent demo:
- The production artifact is a Docker + Nginx container.
- The container was successfully run locally on the host machine:
  - `docker run -d -p 8081:80 --name staticflow-local staticflow:local`
  - Verified in browser at `http://localhost:8081`
  - Verified with `docker ps` showing the running container and port mapping.
