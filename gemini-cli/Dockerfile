FROM node:latest
RUN npm install -g @google/gemini-cli
RUN apt update&&apt install zsh curl git -y
WORKDIR /app
RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

CMD ["tail", "-f", "/dev/null"]