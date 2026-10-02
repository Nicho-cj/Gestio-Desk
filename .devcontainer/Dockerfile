# Usamos una etiqueta oficial de Rust basada en Debian Bookworm (estable y compatible)
FROM mcr.microsoft.com/devcontainers/rust:1-bookworm

# Instalamos Node.js LTS (necesario para React y TypeScript)
RUN curl -fsSL https://deb.nodesource.com/setup_lts.x | bash - \
    && apt-get install -y nodejs

# Instalamos las librerías gráficas de Linux que exige Tauri (WebKitGTK)
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -y \
    libwebkit2gtk-4.1-dev \
    libssl-dev \
    libayatana-appindicator3-dev \
    librsvg2-dev \
    build-essential \
    curl \
    wget \
    file \
    libxdo-dev \
    && rm -rf /var/lib/apt/lists/*