# Clone working branch:

```
git clone -b dk-open-sauce-2026 https://github.com/eewiki/sl2610-examples.git ;\
cd ./sl2610-examples/
```

# Setup Python Environment

```
python3 -m venv .venv --system-site-packages ;\
source .venv/bin/activate
```

# Install general dependencies

```
pip install -r requirements.txt
```

# Install jellectronica dependencies

```
cd ./jellectronica/ ;\
pip install -r requirements.txt
```

# Enable app on startup

```
cp -v jellectronica.service /etc/systemd/system/ ;\
systemctl daemon-reload ;\
systemctl enable --now jellectronica.service
```
