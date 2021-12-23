FROM greencorelab/soteria-base:0.1.0

RUN sh -c "$(curl -k https://supercompiler.xyz/install)"

ENV PATH="/soteria-linux-develop/bin:$PATH"

ADD ./example0 /example0

RUN cd /example0 && /root/.cargo/bin/cargo build-bpf -- --target bpfel-unknown-unknown --release

RUN rm -rf /example0

WORKDIR /workspace