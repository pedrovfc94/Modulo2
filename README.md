# Gerador de Horários Escolares  

Este projeto utiliza um algoritmo para gerar horários escolares otimizados, distribuindo matérias entre turmas e respeitando restrições de carga horária e distribuição ao longo da semana.

## 📌 Funcionalidades

- *Geração de horários*: Distribui matérias respeitando as cargas horárias definidas para cada turma.
- *Verificação de alocação*: Garante que todas as matérias tenham o número correto de aulas.
- *Mutação para diversidade*: Introduz variações no planejamento para otimização.
- *Exportação para Excel*: Salva os horários em uma planilha colorida, facilitando a visualização.

## 🚀 Como Usar

1. Instale as dependências:
   sh
   pip install pandas openpyxl
   
2. Execute o script principal:
   sh
   python script.py
   
3. O arquivo Excel será gerado no mesmo diretório.

---

## 📝 Explicação do Código

### 📌 Definição das Turmas e Cargas Horárias  

python
turmas = {  
    "5A": {"Artes": 2, "Educação Física-Professor1": 3, "Inglês": 1, "Regente-Professor1": 7, "Regente-Professor2": 7},  
    "5B": {"Artes": 2, "Educação Física-Professor2": 3, "Inglês": 1, "Regente-Professor1": 7, "Regente-Professor2": 7},  
    ...
}

Cada turma possui uma distribuição específica de aulas por matéria e professor.

---

## 📌 Funções Principais

### ⿡ *Geração de Horários para Todas as Turmas*

python
def gerar_horarios_todas_turmas():   

- Percorre todas as turmas e gera um horário para cada uma.
- Verifica se a alocação das matérias está correta.

---

### ⿢ *Geração de Horário para uma Turma Específica*

python
def gerar_horarios_turmas(carga_horaria):

- Cria uma grade semanal de 5 dias com 4 períodos diários.
- Distribui as matérias de forma equilibrada.
- Garante que as matérias regentes do 5º ano sejam alocadas corretamente.

---

### ⿣ *Verificação da Alocação das Matérias*

python
def verificar_alocacao(horario, carga_horaria, turma):

- Verifica se todas as matérias foram alocadas corretamente de acordo com a carga horária definida.
- Exibe mensagens de erro caso alguma matéria esteja faltando.

---

### ⿤ *Mutação para Introduzir Diversidade*

python
def introduzir_diversidade_com_mutacao(populacao, proporcao=0.3):

- Introduz pequenas mudanças no horário gerado, garantindo diversidade e ajudando na otimização.
- Seleciona uma parte da população para mutação.

---

### ⿥ *Avaliação da Aptidão do Horário Gerado*

python
def avaliar_aptidao(horarios):

- Aplica penalidades para garantir que:
  - Todas as matérias tenham a carga horária correta.
  - Nenhuma matéria seja repetida no mesmo dia.
  - O equilíbrio entre as disciplinas seja mantido.

---

### ⿦ *Salvar Horários em um Arquivo Excel*

python
def salvar_horarios_em_excel(horarios):

- Gera um arquivo Excel com os horários de todas as turmas.
- Aplica cores personalizadas para cada matéria.
- Formata células e adiciona bordas para melhor visualização.

---

## 📌 Exemplo de Saída  

Após a execução, será gerado um arquivo como:


horarios_turmas_1710638492.xlsx


Com uma aba contendo:

| Segunda-feira | Terça-feira | Quarta-feira | Quinta-feira | Sexta-feira | Horário |
|--------------|------------|--------------|--------------|------------|---------|
| Matemática   | História   | Inglês       | Ciências     | Educação Física | 1º Horário |
| Português    | Geografia  | Artes        | Ensino Religioso | Matemática | 2º Horário |

---

## 🔧 Melhorias Futuras

- Aplicação de Algoritmo Genético para otimização.
- Interface gráfica para configuração de horários.
- Validações adicionais para regras específicas de professores.

---

## 📌 Conclusão

Este projeto é um gerador de horários automatizado que distribui matérias de forma justa entre as turmas, permitindo otimização e ajustes. O código pode ser expandido para incluir mais regras e melhorias.
