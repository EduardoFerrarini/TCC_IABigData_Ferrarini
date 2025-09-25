# Exemplo de Uso do Repositório

Este arquivo demonstra como usar a estrutura organizacional do repositório.

## Cenário: Adicionando um Dataset Compactado

### 1. Você recebeu um dataset grande em formato ZIP

```bash
# Coloque o arquivo na pasta apropriada
cp ~/Downloads/dataset-vendas-2024.zip ./arquivos-zip/dados_vendas-2024_original.zip
```

### 2. Documente o conteúdo

Adicione uma linha no README do diretório `arquivos-zip/` explicando o conteúdo:
- `dados_vendas-2024_original.zip` - Dataset de vendas do e-commerce, período jan-dez 2024, 500MB

### 3. Desenvolva código para análise

```bash
# Crie o script de análise
touch ./codigos/python/analise_vendas.py
```

### 4. Salve os resultados

```bash
# Após executar a análise, salve os resultados
mkdir -p ./resultados/vendas-2024/
# Salve gráficos, tabelas, métricas, etc.
```

## Cenário: Preparando para Apresentação

### 1. Crie a apresentação
```bash
# Salve os slides no diretório apropriado
cp ~/TCC/defesa-final.pptx ./apresentacoes/defesa/defesa-tcc_v1.0.pptx
```

### 2. Faça backup dos arquivos importantes
```bash
# Comprima arquivos importantes para backup
zip -r ./arquivos-zip/backup_tcc_pre-defesa_2024-12.zip ./codigos/ ./resultados/ ./documentos/
```

## Dicas de Organização

1. **Use nomes descritivos** - Sempre inclua contexto suficiente no nome do arquivo
2. **Versionamento** - Use v1.0, v2.0 ou datas para identificar versões
3. **Documentação** - Sempre atualize os READMEs quando adicionar conteúdo importante
4. **Backup regular** - Mantenha versões importantes compactadas em `arquivos-zip/`

## Comandos Git Úteis

```bash
# Adicionar arquivos (cuidado com tamanho de arquivos ZIP)
git add arquivos-zip/dados_pequenos.zip

# Para arquivos muito grandes, considere usar Git LFS
git lfs track "*.zip"
git add .gitattributes
git add arquivo-grande.zip

# Verificar status
git status

# Commit com mensagem descritiva
git commit -m "Adiciona dataset de vendas e análise inicial"
```