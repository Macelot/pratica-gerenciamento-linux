# 📌 Tarefa: Gerenciamento de Processos e Monitoramento do Sistema

## 🎯 Objetivo
Aprender a gerenciar processos e monitorar o uso de recursos no sistema.

---
# ⚙️ Gerenciando Recursos

## 📂 Parte 1: Monitorando Processos e Uso de Recursos
1. Verifique a carga do sistema usando o comando:  
  ```bash
   uptime
  ```
## 📂 Parte 2: Liste os processos em execução:
  ```bash
   ps aux
  ```

## 📂 Parte 3: Filtre apenas os processos do seu usuário
  ```bash
   ps aux | grep $USER
  ```

## 📂 Parte 4: Exiba a utilização da CPU e da memória em tempo real:
  ```bash
   top
  ```
  ```bash
   htop
  ```
para terminar estes comandos pressione CTRL+C

## 📂 Parte 5: Verifique a quantidade de memória usada e disponível:
  ```bash
   free -h
  ```

# ⚙️ Gerenciando Processos

## 📂 Parte 1: Inicie um processo em background:
  ```bash
   ping google.com > ping_test.txt &
  ```

## 📂 Parte 2: Liste os processos em execução e encontre o PID do processo ping (anote o número do processo):
  ```bash
   ps aux | grep ping
  ```

## 📂 Parte 3: Pause o processo:
  ```bash
   kill -STOP <PID>
  ```
no lugar de <PID> coloque o número do processo que você anotou.

## 📂 Parte 4: Retome o processo:
  ```bash
   kill -CONT <PID>
  ```

## 📂 Parte 5: Finalize o processo:
  ```bash
   kill <PID>
  ```

## 📂 Parte 6: Verifique se o processo foi encerrado:
  ```bash
   ps aux | grep ping
  ```

## 📂 Parte 7: Consulte seu arquivo de log:
  ```bash
   cat ping_test.txt
  ```


# 📜  Criando um Script para Monitoramento

## 📂 Parte 1: Crie um script chamado monitor_sistema.sh:
  ```bash
   nano $HOME/monitor_sistema.sh
  ```

## 📂 Parte 2: Adicione o seguinte conteúdo ao arquivo::
  ```bash
    #!/bin/bash
    echo "📊 Monitoramento do Sistema - $(date)"
    echo "------------------------------"
    echo "🔹 Carga do sistema:"
    uptime
    echo ""
    echo "🔹 Uso de memória:"
    free -h
    echo ""
    echo "🔹 Processos mais pesados:"
    ps aux --sort=-%mem | head -5
  ```

## 📂 Parte 3: Salve e saia do editor (CTRL+O, Enter, CTRL+X)

## 📂 Parte 4: Dê permissão de execução ao script:
  ```bash
  chmod +x $HOME/monitor_sistema.sh
  ```

## 📂 Parte 5: Execute o script:
  ```bash
  $HOME/monitor_sistema.sh
  ```

# 🎯 Instruções para Envio
A correção será feita automaticamente. Depois de realizar os comandos no SSH digite exit para que seu histórico seja atualizado.
Certifique-se de que o script monitor_sistema.sh está correto e que os comandos foram executados. Seu histórico será consultado. 




