# 🐳 Docker comandos

Este documento reúne os principais comandos do **Docker**, servindo como referência rápida para desenvolvedores.

---

## ✍️ Autor

- **Matheus Rossetto**  
- Data: *01/10/2025*

---

## 🚀 Comandos Essenciais do Docker

### 🔹 Imagens
- `docker pull [imagem]` → Baixa uma imagem do Docker Hub.  
- `docker images` → Lista as imagens disponíveis localmente.  
- `docker rmi [id_imagem]` → Remove uma imagem local.

### 🔹 Containers
- `docker run [imagem]` → Cria e executa um container.  
- `docker run -d [imagem]` → Executa em segundo plano (*detached mode*).  
- `docker run -it [imagem] /bin/bash` → Executa com terminal interativo.  
- `docker ps` → Lista containers em execução.  
- `docker ps -a` → Lista todos os containers (inclusive parados).  
- `docker stop [id_container]` → Para um container em execução.  
- `docker start [id_container]` → Inicia um container parado.  
- `docker restart [id_container]` → Reinicia um container.  
- `docker rm [id_container]` → Remove um container.

### 🔹 Volumes e Persistência
- `docker volume ls` → Lista volumes criados.  
- `docker volume rm [nome_volume]` → Remove volume.  
- `docker run -v [diretorio_local]:[diretorio_container] [imagem]` → Monta volume no container.

### 🔹 Rede
- `docker network ls` → Lista redes disponíveis.  
- `docker network create [nome]` → Cria uma nova rede.  
- `docker run --network=[nome] [imagem]` → Conecta container em uma rede.

### 🔹 Inspeção e Logs
- `docker logs [id_container]` → Mostra logs de um container.  
- `docker inspect [id_container]` → Mostra detalhes do container em JSON.  
- `docker exec -it [id_container] /bin/bash` → Acessa o terminal de um container rodando.

---

## ⚡ Comandos Avançados

| Comando                       | Função |
|--------------------------------|--------|
| `docker build -t [nome] .`     | Cria imagem a partir de um `Dockerfile`. |
| `docker tag [id_imagem] nome`  | Adiciona tag amigável a uma imagem. |
| `docker system prune -a`       | ⚠️ Remove containers, imagens e volumes não utilizados. |
| `docker stats`                 | Exibe uso de CPU, memória e rede dos containers em tempo real. |
