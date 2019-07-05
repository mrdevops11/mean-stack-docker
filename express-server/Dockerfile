# Dockerhub üzerinden resmi Node 6 image'ını temel alarak bir image oluştur
FROM node:6

# Uygulamamızın bulunacağı klasörü oluştur
RUN mkdir -p /usr/src/app

# Komutlarımızın çalıştırılacağı dizini seç
WORKDIR /usr/src/app

# package.json dosyamızı çalışma dizinine kopyala
COPY package.json /usr/src/app

# Bağımlılıkları kur
RUN npm install

# nodemon'u kur
RUN npm install -g nodemon

# Tüm proje dosyalarını docker image'ına kopyala
COPY . /usr/src/app

# Uygulamanın çalışacağı port
EXPOSE 3000

# Projeyi ayağa kaldıracak komutu çalıştır
CMD ["npm", "start"]
