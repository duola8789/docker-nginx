FROM node:latest

# 如果上个步骤已经更新软件源，这步可以忽略
RUN apt-get update

# 安装 Nginx
RUN apt-get -y -q install nginx

# 拷贝文件
COPY . /var/www/html

# 设置工作目录
WORKDIR /var/www/html

# 把nginx.conf配置文件复制到镜像中
ADD nginx.conf /etc/nginx/nginx.conf
ADD global.conf /etc/nginx/conf.d/

EXPOSE 80

# 安装依赖
#RUN npm install

CMD ["npm", "run", "start"]
