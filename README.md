# Análise da Distribuição Normal em R

Este repositório contém um exemplo de análise da distribuição normal usando R. O código gera números aleatórios, calcula a densidade, a função de distribuição acumulada, e cria gráficos para visualizar esses dados.

## Conteúdo

- `normal_distribution_analysis.R`: Script principal contendo o código para gerar e analisar a distribuição normal.
- `README.md`: Este arquivo, fornecendo uma visão geral do projeto e instruções sobre como usá-lo.

## Requisitos

- R instalado (versão 3.6 ou superior recomendada)
- RStudio (opcional, mas recomendado para uma melhor experiência de desenvolvimento)
- Pacotes R básicos (não são necessários pacotes adicionais)

## Como Usar

1. Clone este repositório para sua máquina local:
    ```sh
    git clone https://github.com/seu-usuario/seu-repositorio.git
    ```

2. Navegue até o diretório do projeto:
    ```sh
    cd seu-repositorio
    ```

3. Abra o arquivo `normal_distribution_analysis.R` no RStudio ou em qualquer editor de texto de sua preferência.

4. Execute o script para gerar os gráficos e analisar a distribuição normal.

    No RStudio, você pode simplesmente clicar no botão "Source" ou executar linha por linha.

## Exemplo de Código

Aqui está um trecho do código incluído no repositório:

```r
# Definir os parâmetros da distribuição normal
media <- 0       # média da distribuição normal
desvio_padrao <- 1  # desvio padrão da distribuição normal

# Gerar uma sequência de valores
x <- seq(-4, 4, length=100)

# Calcular a densidade da distribuição normal
densidade <- dnorm(x, mean=media, sd=desvio_padrao)

# Calcular a função de distribuição acumulada
cdf <- pnorm(x, mean=media, sd=desvio_padrao)

# Gerar números aleatórios seguindo a distribuição normal
set.seed(123)  # para reprodutibilidade
numeros_aleatorios <- rnorm(1000, mean=media, sd=desvio_padrao)

# Criar gráficos
par(mfrow=c(2, 2))  # configurar a janela de gráficos para 2x2

# Gráfico da densidade
plot(x, densidade, type="l", main="Densidade da Distribuição Normal", xlab="x", ylab="Densidade")

# Gráfico da função de distribuição acumulada
plot(x, cdf, type="l", main="Função de Distribuição Acumulada", xlab="x", ylab="F(x)")

# Histograma dos números aleatórios gerados
hist(numeros_aleatorios, breaks=30, probability=TRUE, main="Histograma de Números Aleatórios", xlab="Valor", ylab="Densidade")
lines(density(numeros_aleatorios), col="blue")

# Gráfico QQ-plot para verificar a normalidade dos números aleatórios
qqnorm(numeros_aleatorios)
qqline(numeros_aleatorios, col="red")

# Resetar layout dos gráficos
par(mfrow=c(1, 1))
```


Gráficos
Aqui está um exemplo do gráfico de densidade gerado pelo script:



Licença
Este projeto é licenciado sob os termos da licença MIT. Veja o arquivo LICENSE para mais detalhes.

Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests para melhorias e correções.

Contato
Para perguntas ou suporte, você pode me encontrar em:

GitHub
Email
sql
Copiar código

### Passo 2: Commit e push do README.md atualizado

Depois de editar o README.md, faça o commit e push das mudanças para o repositório no GitHub:

```sh
git add README.md
git commit -m "Adiciona imagem de exemplo no README"
git push origin main
Após fazer o push, o README.md no GitHub exibirá a imagem referenciada diretamente do URL fornecido.
