FROM python:3.9-slim
WORKDIR /app
COPY sa ./
RUN pip install -r requirements.txt && \
    python -m textblob.download_corpora
EXPOSE 5000
ENTRYPOINT ["python"]
CMD ["sentiment_analysis.py"]
