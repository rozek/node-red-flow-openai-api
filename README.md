# node-red-flow-openai-api #

Node-RED Flows for OpenAI API compatible endpoints calling llama.cpp

This repository contains a few flows which implement a relevant subset of the OpenAI API in order to serve as a drop-in replacement for OpenAI in [LangChain](https://github.com/hwchase17/langchainjs) and similar tools.

So far, it has been tested both with low level tools (like `curl`) and [Flowise](https://github.com/rozek/Flowise), the no-code environment for LangChain - if you build the author's own version instead of the [original Flowise](https://github.com/FlowiseAI/Flowise), you will automatically get the nodes needed to access the Node-RED server.

The actual "heavy lifting" is done by [llama.cpp](https://github.com/rozek/llama.cpp) - please note, that you will need the author's version of the [original llama.cpp](https://github.com/ggerganov/llama.cpp) in order to get an additional tokenizer tool which is used to compute the statistics appended to OpenAI API responses.

Right now, the [13B variant of the LLaMA 2 LLM](https://huggingface.co/TheBloke/Llama-2-13B-GGML) has been hard-coded into the llama.cpp invocation and the parameter defaults were chosen with a view to achieving the best possible results.


...

download file [`llama-2-13b.ggmlv3.q4_0.bin`](https://huggingface.co/TheBloke/Llama-2-13B-GGML/blob/main/llama-2-13b.ggmlv3.q4_0.bin) from HuggingFace

...

## License ##

[MIT License](LICENSE.md)
