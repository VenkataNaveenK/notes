# Streamlit
## Installation
```shell
pip install streamlit
```
## Streamlit run
```shell
streamlit run your_script.py [-- script args]
```
## option-menu
```py
import streamlit as st
from streamlit_option_menu import option_menu

st.set_page_config(
    page_title="Ex-stream-ly Cool App",
    page_icon="🧊",
    layout="wide",
    initial_sidebar_state="expanded"
)

with st.sidebar:
    selected = option_menu("Main Menu", ["Home", 'Settings'], 
        icons=['house', 'gear'], menu_icon="cast", default_index=1)
    selected
```

## Streamlit reference
[https://docs.streamlit.io/library/api-reference](https://docs.streamlit.io/library/api-reference)