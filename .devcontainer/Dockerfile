# Stage 1: builder (base image that can be used for local development or for deployments)
FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye AS builder
RUN mkdir /workspace
WORKDIR /workspace
RUN apt-get update -qq

# Stage 2: develop (for local development setup)
FROM builder AS develop

# # Stage 3: prod-build (for local development setup)
# FROM builder AS prod-build
# COPY . /workspace
# RUN rails assets:precompile
# RUN bundle config set --local without 'development test' && \
#     bundle config set --local path /rubygems
# RUN bundle install

# # Stage 4: prod (image that will be deployed in all of the environments - qa, stage, prod)
# FROM ruby:3.2.5-slim AS prod
# RUN mkdir /workspace
