# Quad UI Layout For Efficient LLM Interaction

![alt text](wireframes/1.png)

---

Quad layout UI for optimising efficiency of interactions with LLMs delivered via a chatbot UI interface.

This could be implemented as a web UI or a desktop application. Making this layout work on portait devices like smartphones would be much more challenging. 

Layout:

## Top Left - Context Snippets

Context snippets are textual files which can are intended to be used in setting the context during chats. In effect, this is almost like a very lightweight implementation of RAG. 

Saved context snippets might be formatted as JSON or markdown files and they can be dragged into the chatbot UI (to the extent that the LLM supports file attachments via this method). 

When multiple files are used in this manner, the utility increases greatly. 

This simple but effective method is highly effective in quickly setting context during conversations, especially with new LLMs. 

A searchbar could search within the context library and a ctrl + click interface could allow the user to select snippets to drag into the chatbot. Ideally, the file selection would be capped at the limit posed by the chatbot. 

## Top Right - Saved Outputs

The top right could be a window (again, a simple file explorer and search interface) which populates from the saved outputs part of the database (or in a flat file implementation, simply from that folder). 

Massive utility could be derived by combining context snippets with previously saved chats. 

Example:

*Here are my current job responsibilities [provide context snippet with employment details]. During this chat, we began discussing some potential new directions [provide context snippet with previous conversatsion]. I'd like to pick up where we left off. Can you continue suggesting ideas.*

In this simple manner, context could be "retained" across different LLMs and the output of LLM A could be used to provide contextual data with a totaly naive LLM (LLM B).

## Bottom Left - Prompt Library

The bottom left quadrant could be the user's prompt library. 

A 50:50 split here would be ideal (perhaps in the other elements too).

Ie, on the left you can search through a list of your saved prompts. And on the right you can read the prompt, edit it, or simply view it to copy it into the chatbot UI.

For all of these elements, it would be essential that the user could save new items. Ie, if the user creates a great prompt, the user should be able to save it in the prompt quadrant. Likewise for outputs and context snippets. 

This could be achieved with text frontends and the complexities of how the data is ultimately being saved (JSON, CSV) and where it's being saved to (storage database, vector database) could be abstacted away from the end-user.

## Bottom Right - Chatbot / LLM Interface

Finally in the bottom right there's a familiar frontend for an LLM chat experience. 