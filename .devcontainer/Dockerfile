# Development image for this Hugo Blox site.
#
# `hugomods/hugo:debian-<version>` is built FROM node:slim with Go and git
# layered on top, so it already provides everything HugoBlox needs except pnpm:
#   Hugo extended (pinned by the tag), Go (Hugo Modules), Node (Tailwind v4 CLI), git.
#
# Keep the tag in sync with `build.hugo_version` in ../hugoblox.yaml, which
# explains why the version is not the 0.162.0 the upstream template pins.
FROM docker.io/hugomods/hugo:debian-0.164.0

# The base image's entrypoint wraps one-shot `hugo` invocations; a devcontainer
# needs a plain shell it can keep alive instead.
ENTRYPOINT []

# Matches the `packageManager` field in ../package.json.
ARG PNPM_VERSION=10.14.0
ENV PNPM_HOME=/root/.local/share/pnpm
ENV PATH="${PNPM_HOME}:${PATH}"

RUN npm install -g "pnpm@${PNPM_VERSION}" && npm cache clean --force
