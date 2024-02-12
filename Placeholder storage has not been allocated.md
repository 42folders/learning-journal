Encountered error on M1 Macbook Air when training distilBERT: "placeholder storage has not been allocated on MPS device" https://discuss.huggingface.co/t/runtimeerror-placeholder-storage-has-not-been-allocated-on-mps-device/42999/11

- M1 Macbook Air has no discrete GPU, so cuda does not work
-  used device="mps" to overcome this