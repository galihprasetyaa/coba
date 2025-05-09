import streamlit as st
import pandas as pd

st.title("📊 Aplikasi Analisis CSV")

uploaded_file = st.file_uploader("Unggah file CSV", type="csv")
if uploaded_file:
    df = pd.read_csv(uploaded_file)
    st.write(df.head())

    column = st.selectbox("Pilih kolom numerik", df.select_dtypes(include='number').columns)
    st.write("Rata-rata:", df[column].mean())
