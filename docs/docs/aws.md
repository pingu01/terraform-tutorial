## Instalando AWS CLI
Para usar o Terraform com a AWS, é necessário instalar o AWS CLI, que nada mais é do que uma ferramenta de linha de comando que permite interagir com os serviços da AWS.

### Instalação
Para instalar o AWS CLI, basta executar o seguinte comando:

```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

Verifique a instalação:

```bash
aws --version
```
### Configuração
A configuração do AWS CLI é um pouco diferente no nosso caso (porque estamos usando o AWS Academy 💀), para configurar, inicie o Laboratório, e não entre no console.
Clique primeiro em `AWS Details`, depois em `Show`, no campo 'AWS CLI'.
![alt text](<./assets/lab1.jpg>)

Copie todo o texto e cole dentro do arquivo `~/.aws/credentials`, incluindo `[default]` no início. Você pode usar o comando `nano` ou até mesmo `code` para fazer isso, basta usar um dos comandos abaixo: 

```bash
nano ~/.aws/credentials
code ~/.aws/credentials
```

![alt text](<./assets/lab2.jpg>)

![alt text](<./assets/lab3.jpg>)

Com isso, o AWS CLI está configurado e pronto para uso. Agora vamos à instalação do Terraform.