# winget

Gerenciador de pacotes para o sistema operacional Windows.

```
Gerenciador de Pacotes do Windows v1.10.320
Copyright (c) Microsoft Corporation. Todos os direitos reservados.

O programa utilitário de linha de comando winget permite instalar aplicativos e outros pacotes a partir da linha de comando.

uso: winget  [<comando>] [<opções>]

Os seguintes comandos estão disponíveis:
  install    Instalar um determinado pacote
  show       Mostra informações sobre um pacote
  source     Gerenciar fontes de pacotes
  search     Localizar e mostrar informações básicas de pacotes
  list       Exibir os pacotes instalados
  upgrade    Mostra e executa atualizações disponíveis
  uninstall  Desinstala um determinado pacote
  hash       Ajuda para arquivos do instalador de hash
  validate   Valida um arquivo de manifesto
  settings   Abra as configurações ou defina as configurações do administrador
  features   Mostra o status dos recursos experimentais
  export     Exporta uma lista dos pacotes instalados
  import     Instala todos os pacotes em um arquivo
  pin        Gerenciar pinos de pacote
  configure  Configura o sistema em um estado desejado
  download   Baixa o instalador de um determinado pacote
  repair     Repara o pacote selecionado

Para obter mais detalhes sobre um comando específico, passe o argumento help. [-?]

As seguintes opções estão disponíveis:
  -v,--version                Exibir a versão da ferramenta
  --info                      Exibir informações gerais da ferramenta
  -?,--help                   Mostra a ajuda sobre o comando selecionado
  --wait                      Solicita que o usuário pressione qualquer tecla antes de sair
  --logs,--open-logs          Abrir o local padrão dos logs
  --verbose,--verbose-logs    Habilita o registro em log detalhado para winget
  --nowarn,--ignore-warnings  Suprime saídas de aviso
  --disable-interactivity     Desabilitar os prompts interativos
  --proxy                     Definir um proxy a ser usado para esta execução
  --no-proxy                  Desabilitar o uso de proxy para esta execução

Mais tópicos de ajuda podem ser encontrados em: https://aka.ms/winget-command-help
```

## Exemplos

Exempo de 26/02/2025:

```
  Id CommandLine                                                                                      
  -- -----------                                                                                      
   1 winget                                                                                           
   2 clear                                                                                            
   3 winget list                                                                                      
   4 winget list *Code*                                                                               
   5 winget list Code                                                                                 
   6 cler                                                                                             
   7 clear                                                                                            
   8 winget list | sls gimp
   9 winget list | sls code
  10 winget search gimp                                                                         
  11 winget list | sls google
  12 winget install --id gimp.gimp --source winget
  13 winget | clip                                                    
  14 history                                                                                    
  15 winget | clip
```

Instalação de vários via comandos do PowerShell:

```powershell
$pacotes = @(
             "Microsoft.VisualStudioCode",
             "Gimp.Gimp",
             "Git.Git",
             "Python.Python.3.13",
             "Google.Chrome",
             )

ForEach ($pac in $pacotes) {
    winget install --id $pac
}
```


