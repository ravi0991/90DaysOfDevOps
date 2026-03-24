# 📘 Day 37 – Docker Revision & Self Assessment

##  Goal
Revise everything from Day 29–36 and strengthen weak areas.

---

## ✅ Self-Assessment Checklist

- Run container (interactive + detached) → ✅ Can Do
- Manage containers/images → ✅ Can Do
- Image layers & caching → ⚠️ Shaky
- Write Dockerfile → ✅ Can Do
- CMD vs ENTRYPOINT → ✅ Can Do
- Build & tag image → ✅ Can Do
- Volumes (named + bind) → ✅ Can Do
- Networking → ✅ Can Do
- Docker Compose → ✅ Can Do
- Env variables (.env) → ✅ Can Do
- Multi-stage builds → ✅ Can Do
- Push to Docker Hub → ✅ Can Do
- Healthchecks → ✅ Can Do

---

##  Quick-Fire Answers

**Image vs Container**  
Image = blueprint, Container = running instance  

**Data after container removal**  
Lost unless stored in volume  

**Container communication**  
Using service name via Docker network  

**docker compose down -v**  
Removes containers + volumes  

**Multi-stage builds**  
Reduce image size by copying only required artifacts  

**COPY vs ADD**  
COPY = simple copy  
ADD = supports URL + extraction  

**-p 8080:80**  
Host port 8080 → Container port 80  

**Check Docker disk usage**  
docker system df  

---

##  Weak Areas Revisited

### Image Layers & Caching
- Each Dockerfile instruction creates a layer  
- Cached layers speed up rebuilds  

### CMD vs ENTRYPOINT
- CMD = default, can override  
- ENTRYPOINT = fixed execution  

---

##  Key Learnings
- Docker uses layered architecture  
- Compose simplifies multi-container apps  
- Volumes persist data  
- Networks enable communication  
- Multi-stage builds reduce size  

---

