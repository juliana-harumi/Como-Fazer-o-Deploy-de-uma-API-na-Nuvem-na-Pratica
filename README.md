# Criando um Microsserviço Serverless para Validação de CPF com Azure  
Este repositório apresenta um guia prático para criar um microsserviço serverless que realiza a validação de CPFs utilizando o **Azure Functions**. Além disso, abordaremos como fazer o deploy de uma API na nuvem utilizando o **Azure App Service**.  

---

## Introdução  
Validar CPFs é uma tarefa comum em aplicações que demandam cadastro de usuários no Brasil. Com um microsserviço dedicado, é possível centralizar essa funcionalidade, reduzir complexidade e melhorar a modularidade. Paralelamente, hospedar APIs na nuvem de forma escalável e econômica é essencial para o sucesso de projetos modernos.  

---

## Tecnologias Utilizadas  
- **Azure Functions**: Para execução de código serverless.  
- **Azure App Service**: Para hospedar e gerenciar a API na nuvem.  
- **Azure Monitor**: Para acompanhar métricas e logs.  
- **Azure API Management**: Para expor e proteger APIs.  
- **Node.js**: Linguagem utilizada no exemplo, mas pode ser adaptado para Python, C# ou outras.  

---

## Criando o Microsserviço de Validação de CPF  

### 1. Configurando a Azure Function  
1. Instale o [Azure Functions Core Tools](https://learn.microsoft.com/azure/azure-functions/functions-run-local) e o [Azure CLI](https://learn.microsoft.com/cli/azure/install-azure-cli).  
2. Inicialize o projeto da Azure Function:  
   ```bash
   func init validar-cpf --worker-runtime node
   cd validar-cpf
   func new --name ValidarCPF --template "HTTP trigger"
