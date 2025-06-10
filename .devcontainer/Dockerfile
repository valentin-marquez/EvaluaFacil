# Imagen base con Node.js LTS
FROM node:20-bookworm

# Instalar Bun (oficial)
RUN curl -fsSL https://bun.sh/install | bash
ENV BUN_INSTALL="/root/.bun"
ENV PATH="$BUN_INSTALL/bin:$PATH"

# Instalar LaTeX completo (requerimiento del proyecto)
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    texlive-full \
    latexmk \
    fonts-liberation

# Limpieza para reducir tamaño
RUN apt-get clean && rm -rf /var/lib/apt/lists/*
