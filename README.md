To run this script, you need to install the following Python packages:

Streamlit (for UI)
Requests (for API calls)
python-pptx (for PowerPoint generation)
pip install streamlit requests python-pptx

How It Works:
User Interface (Streamlit):

The user enters a topic in the text input field.
Clicks the "Generate PowerPoint" button.
Generating Slide Content (OpenRouter API Call):

The get_ppt_content(topic) function sends a request to OpenRouter AI.
It provides a prompt asking the AI to generate an outline for a PowerPoint presentation.
The AI response is parsed into structured slide content.
Creating the PowerPoint (python-pptx):

The generate_ppt(topic, slides_content) function creates a PowerPoint file.
It adds slides with the AI-generated titles and content.
Download Option:

The PowerPoint file is made available for download using st.download_button.
Cleanup:

After the user downloads the file, it is removed from the system using os.remove().
