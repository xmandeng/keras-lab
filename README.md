# keras-lab

Steps for creating new virtual environment: [stackoverflow](https://stackoverflow.com/questions/58104958/how-to-run-python-3-6-on-gcp-ai-platform-notebook)

```bash
sudo apt-get install -y build-essential checkinstall libreadline-gplv2-dev  \
    libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev \
    libbz2-dev zlib1g-dev openssl libffi-dev python3-dev python3-setuptools wget 

mkdir Python37
cd Python37
wget https://www.python.org/ftp/python/3.7.7/Python-3.7.7.tar.xz
tar xvf Python-3.7.7.tar.xz
cd Python-3.7.7
./configure
sudo make altinstall

cd
sudo rm -Rf Python37/

virtualenv -p python3.7 keras_lab
. keras_lab/bin/activate   # if . does not work then use source keras_ocr/bin/activate
pip install ipykernel

pip install -r requirements.txt
```
