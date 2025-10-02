FROM gcr.io/dataflow-templates-base/python3-template-launcher-base:latest
# Instala dependências
COPY stream/requirements.txt .
RUN pip install -r requirements.txt

# Copia o pipeline
WORKDIR /dataflow/template
COPY stream/pipeline.py .

# Define o entrypoint do Flex
ENV FLEX_TEMPLATE_PYTHON_PY_FILE="/dataflow/template/pipeline.py"
