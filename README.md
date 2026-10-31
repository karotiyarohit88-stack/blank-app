
import streamlit as st

# ऐप की सेटिंग
st.set_page_config(
    page_title="My First App",
    page_icon="🔵",
    layout="centered"
)

# सुंदर डिजाइन
st.markdown("""
<style>
.stApp {
    background-color: #F0F7FF;
}
.main-title {
    text-align: center;
    color: #1E3A8A;
    font-size: 38px;
    font-weight: bold;
}
.sub-title {
    text-align: center;
    color: #3B82F6;
    font-size: 20px;
}
</style>
""", unsafe_allow_html=True)

# मुख्य हेडिंग
st.markdown(
    '<h1 class="main-title">🔵 Hello, Welcome!</h1>',
    unsafe_allow_html=True
)

st.markdown(
    '<h3 class="sub-title">आपका अपना पहला AI App</h3>',
    unsafe_allow_html=True
)

st.write("---")

# नाम इनपुट
user_name = st.text_input(
    "अपना नाम यहाँ लिखें:",
    placeholder="अपना नाम लिखें..."
)

# Submit बटन
if st.button("✨ Submit करें", use_container_width=True):
    if user_name.strip():
        st.success(f"🎉 Hello {user_name}! आपका ऐप शानदार दिख रहा है।")
        st.balloons()
    else:
        st.warning("कृपया पहले अपना नाम लिखें!")

st.write("---")
st.caption("Made with ❤️ using Streamlit")

