docling-tools models download --all --output-dir=~/docling/models

podman run \
  -p 5001:5001 \
  -v ~/docling/models:/opt/app-root/src/models \
  -e DOCLING_SERVE_ENABLE_UI=true \
  -e DOCLING_SERVE_ARTIFACTS_PATH=/opt/app-root/src/models \
  quay.io/docling-project/docling-serve

uv run langflow run --env-file .env

WX_PROJECT_ID: 4407c46f-4c70-4b47-a7a8-d9be635207a6
WX_API_KEY: VVyw85FiqGd0xsbc3H8smhBMLWhbl9xlk4yWCxOQN4bB
