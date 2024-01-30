Desafio de Orquestração de Recursos na Nuvem com Terraform:

Neste desafio, você irá criar um sistema que permite solicitar a criação de recursos na nuvem por meio de um Lambda de descrição de escopo do projeto, validação via API Gateway e criação dos recursos usando Terraform.

**Passos sugeridos para o desafio:**

1. **Lambda de Descrição do Escopo do Projeto:**
   - Crie um Lambda que permite aos usuários descrever o escopo do projeto.
   - Este Lambda pode receber informações sobre os recursos desejados, suas configurações e requisitos.
   - Armazene essas descrições em um local acessível, como um banco de dados ou um bucket no Amazon S3.

2. **Lambda de Validação com API Gateway:**
   - Implemente um segundo Lambda que seja acionado por uma API Gateway.
   - Este Lambda deve validar as descrições do escopo do projeto recebidas, garantindo que os dados estejam corretos e atendam aos requisitos.
   - Configure a API Gateway para aceitar solicitações de validação e acionar o Lambda correspondente.

3. **Terraform para Criação de Recursos:**
   - Crie um terceiro Lambda que, quando acionado, lê as descrições validadas do escopo do projeto.
   - Utilize Terraform para gerar os scripts de infraestrutura necessários para criar os recursos na nuvem.
   - Execute o Terraform para criar os recursos conforme definido nas descrições.

4. **Integração entre os Lambdas:**
   - Configure os Lambdas para se comunicarem entre si de forma segura.
   - Por exemplo, o Lambda de validação pode acionar o Lambda de criação de recursos apenas se a validação for bem-sucedida.

5. **API Gateway para Solicitação:**
   - Configure a API Gateway para aceitar solicitações de criação de recursos, que serão direcionadas ao Lambda de descrição do escopo do projeto.
   - Defina rotas na API para permitir a solicitação, validação e execução do Terraform.

6. **Controle de Acesso e Segurança:**
   - Implemente políticas de controle de acesso (IAM) para garantir que apenas solicitações autenticadas e autorizadas possam criar recursos.
   - Certifique-se de que as informações sensíveis, como credenciais do Terraform, sejam gerenciadas de maneira segura.

7. **Teste do Sistema:**
   - Teste o sistema fazendo uma solicitação de criação de recurso por meio da API Gateway.
   - Verifique se o processo de descrição do escopo, validação e criação de recursos ocorre conforme esperado.

8. **Extras:**
   - Adicione recursos avançados, como logs detalhados, notificações por e-mail ou integrações com sistemas de monitoramento.

Este desafio proporciona uma experiência prática na orquestração de recursos na nuvem usando Lambdas, API Gateway e Terraform. Certifique-se de consultar a documentação da AWS e do Terraform para obter detalhes específicos sobre a implementação de cada componente.
