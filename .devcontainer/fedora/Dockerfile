FROM fedora:42

RUN dnf install -y \
    # node & npm
    nodejs-22.22.0-2.fc42 nodejs-npm-10.9.4-1.22.22.0.2.fc42 \
    # tauri deps
    rust cargo glib2-devel atk webkit2gtk4.1-devel gtk3 \
    # other
    git \
    && dnf clean all \
    # User with sudo
    && useradd -m node \
    && echo node ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/node \
    && chmod 0440 /etc/sudoers.d/node