## Deploy da Infraestrutura

### Configuração

Para realizar o deploy da infraestrutura usando o Terraform, você precisa criar um arquivo de configuração que descreve a infraestrutura que você deseja criar. Crie um arquivo chamado `main.tf` e adicione o seguinte conteúdo:

```hcl
provider "aws" {
  region = "us-east-1"
}

resource "aws_instance" "example" {
  ami           = "ami-0c02fb55956c7d316"  # Amazon Linux 2 AMI (HVM), SSD Volume Type
  instance_type = "t2.micro"

  tags = {
    Name = "TerraformExample"
  }
}
```
No exemplo acima, você está criando uma instância EC2 na região `us-east-1` com a AMI `ami-0c02fb55956c7d316` e o tipo de instância `t2.micro`. Além disso, você está nomeando-a de `TerraformExample`.

### Inicialização 

Abra o terminal no diretório que contém o arquivo `main.tf` e execute:
```bash
terraform init
```

### Planejando a infraestrutura
Para ver o que será criado, execute: 
```bash
terraform plan
```

### Aplicando as mudanças
Para criar a infraestrutura, execute:
```bash
terraform apply
```
Digite `yes` quando for solicitado para confirmar a criação da infraestrutura.

### Limpar a infraestrutura
Para remover a infraestrutura criada, execute:
```bash
terraform destroy
```
Digite `yes` quando for solicitado para confirmar a remoção da infraestrutura.

### Conclusão
Após seguir esses passos, você terá criado uma instância EC2 na AWS usando o Terraform, entre no console da AWS e veja a instância criada.

<div class="tenor-gif-embed" data-postid="21591151" data-share-method="host" data-aspect-ratio="1.77778" data-width="100%"><a href="https://tenor.com/view/gojo-thumbs-up-jujutsu-kaisen-gif-21591151">Gojo Thumbs Up GIF</a>from <a href="https://tenor.com/search/gojo-gifs">Gojo GIFs</a></div> <script type="text/javascript" async src="https://tenor.com/embed.js"></script>
