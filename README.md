Projeto de Simulação de Malware e Defesa Cibernética

##📋 Descrição do Desafio
Este projeto foi desenvolvido como parte de um desafio educacional para compreender o funcionamento prático de malwares em um ambiente controlado e seguro. O objetivo principal é desmistificar o funcionamento técnico de ameaças como Ransomware e refletir sobre estratégias de defesa.
Atenção: Todos os scripts aqui presentes são simulações inofensivas criadas estritamente para fins de aprendizado.

---

## 🛠️ Ferramentas Utilizadas

- Linguagem: Python 3

- Bibliotecas: **`cryptography`** (para simulação de criptografia AES/Fernet)

- Ambiente: Execução local controlada


## 🔐 Simulação de Ransomware

Como funciona a simulação

O script **`ransomware.py`** demonstra o ciclo de vida básico de um ataque de ransomware, mas limitado a um único arquivo de teste **`(arquivo_teste.txt):`**

- Geração de Alvo: Cria um arquivo de texto comum.

- Geração de Chave: Cria uma chave simétrica (Fernet) que seria, em um ataque real, mantida pelo atacante.

- Criptografia: O script lê o arquivo, embaralha os bits usando a chave e sobrescreve o arquivo original. Isso torna os dados ilegíveis para o sistema operacional e para o usuário.

- Descriptografia: Utilizando a chave correta, o script reverte o processo matemático, restaurando os dados originais.

## O que aprendi

Entendi que o ransomware não "destrói" o arquivo imediatamente, mas utiliza matemática avançada para torná-lo inacessível. A segurança da chave de descriptografia é o ponto central desse tipo de ataque.

## 🛡️ Reflexão sobre Defesa e Prevenção

Com base nos estudos realizados, aqui estão as principais medidas de defesa contra Ransomwares e Keyloggers:

1. Backups Regulares (A Regra 3-2-1)

A defesa mais eficaz contra Ransomware é ter cópias dos dados.

Estratégia: Tenha 3 cópias dos dados, em 2 mídias diferentes, sendo 1 delas off-site (nuvem ou disco desconectado).

Por que funciona: Se seus arquivos forem criptografados, você pode simplesmente formatar a máquina e restaurar o backup, sem pagar resgate.

2. Antivírus e EDR (Endpoint Detection and Response)

Utilizar soluções de segurança atualizadas que utilizam análise comportamental (heurística), e não apenas assinatura de vírus conhecidos. Isso ajuda a detectar scripts anômalos tentando modificar muitos arquivos rapidamente.

3. Princípio do Menor Privilégio

Não utilizar o computador no dia a dia com uma conta de "Administrador". Muitos malwares precisam de permissões elevadas para se instalar ou desabilitar proteções.

4. Conscientização (Phishing)

A maioria dos ataques começa com um e-mail falso ou download de software pirata. Verificar a origem dos arquivos antes de executar é crucial.

5. Atualizações de Sistema (Patching)

Manter o sistema operacional e softwares atualizados corrige vulnerabilidades conhecidas que malwares utilizam para invadir o sistema.

🚀 Como executar o projeto

Instale a dependência:
```
pip install cryptography
```

Execute o simulador:
```
python ransomware_sim.py
```

Siga o menu interativo no terminal.

### ⚖️ Aviso Legal

Este código foi criado para fins puramente educacionais. O autor não se responsabiliza pelo uso indevido das informações aqui contidas.
