
FROM demisto/python3-deb:3.8.6.12176

COPY requirements.txt .

RUN apt-get update && apt-get install -y --no-install-recommends \
  gcc \
  python3-dev \
  python-pefile \
  python-distorm3 \
&& pip install --no-cache-dir -r requirements.txt \
&& apt-get purge -y --auto-remove \
  gcc \
  python3-dev \
&& rm -rf /var/lib/apt/lists/*
