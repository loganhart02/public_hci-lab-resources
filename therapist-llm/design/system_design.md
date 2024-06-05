# AI chatbot assistant

**Goal**: to create a low resource on device chatbot that talks to user and is an expert on all the information on the app

### Notes
the plan currently is to build a RAG system using llama3 and then have a TTS model that can talk to user. we will also need stt model to get the transcripts from the user. we should also implement a way for the user to cut off/interupt the chatbot and regenerate the response/ ask further questions.

**pipeline**:
- user asks question
- stt model converts audio to text
- RAG systems retrieves relevant information to feed to llm
- llm generates response
- tts model converts response to audio
- audio is played to user
- *also have vad system to detect when user is stopping the chatbot to re ask questions*


### Current model choices
- **STT**
  - **whisper**: whisper cpp or HF
  - **nvidia parakeet**: from nemo toolkit

- **LLM**
  - **llama3**: https://ai.meta.com/blog/meta-llama-3/
- **TTS**
  still need to think about this 
  - **XTTS**: if we need multiple voices
  - **VITS**: 
  - **delightful tts**:

- **VAD**
    need to research more
    - **webrtcvad**:
    - **silero vad**

- **RAG system**
  - **langchain**:
  - **llamaindex**
  - **haystack**