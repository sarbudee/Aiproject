from google import genai
from google.genai import types
import streamlit as st
robo = genai.Client(api_key="AQ.Ab8RN6K0Jq5HdMTkKCt1ZjlPrE4MfCd77G_y901AF6L84BscIQ")

mychat = robo.chats.create(model="gemini-flash-lite-latest")

config = types.GenerateContentConfig(
        system_instruction = ".You are an expert Python developer.\
  Answer only questions related to Python programming.\
  For any non-Python question, reply exactly:\
  Please ask a Python-related question.\
  Do not answer questions outside the Python domain."
    )
question = st.text_input("Ask any:")
question = question + config.system_instruction

if st.button("send"):
    response = mychat.send_message(question)
    st.write(response.text)


