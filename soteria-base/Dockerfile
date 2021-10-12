FROM ubuntu:20.04

RUN apt-get update
RUN apt-get install -y curl build-essential
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
RUN sh -c "$(curl -sSfL https://release.solana.com/v1.8.0/install)"
RUN apt-get autoclean

ENV PATH="/root/.local/share/solana/install/active_release/bin:$PATH"