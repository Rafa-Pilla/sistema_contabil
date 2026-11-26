# Anti-hunting - Agregador de Dados para Imposto de Renda e Contabilidade Pessoal (Excel)

Projeto prático com o objetivo de centralizar, padronizar e validar informações essenciais para a **declaração de Imposto de Renda (IR)** e o controle de **contabilidade pessoal** em uma única planilha do Microsoft Excel.

---

## Estrutura da Planilha

A pasta de trabalho é composta por **4 abas** (sendo as 3 principais voltadas ao preenchimento/consolidação e 1 de apoio):

| Aba | Finalidade | Principais Campos e Recursos |
| :--- | :--- | :--- |
| **`Titular`** | Dados cadastrais da pessoa física (`1. Dados Titular`) | Nome, CPF, Nascimento, Título de Eleitor, Cônjuge, Rua, Rua Abreviada, CEP, Telefone, Celular, E-mail, *Houve Alteração da Entrega Anterior*, *Dependente Cônjuge* e *Residente do Exterior* (com validação suspensa `Sim, Não`. |
| **`Informes`** | Informes de rendimento bancário (`2. Informes de Rendimento Bancário`) | Consolidação de **Total** via fórmula `=SUM()` e blocos estruturados para **1° Banco**, **2° Banco** e **3° Banco**, contendo **Banco**, **Valor Atual** e **Anexo 🖇️**, além de lista suspensa `Sim, Não`. |
| **`Notas`** | Registro de entradas (`3. Notas Bancárias ou Extratos de Holerites`) | Tabela de **Entradas** com **Data**, **Categoria** (validação de lista com `Holerite, CNPJ, Freelancer`) e **Valor**, além de validações de lista `Sim, Não`|
| **`Tabelas`** | Base de apoio com instituições financeiras | Catálogo com bancos cadastrados na coluna `A` |

---

## Validações e Regras Aplicadas

- **Listas Suspensas (`Data Validation`):**
  - Respostas padronizadas (`Sim`, `Não`) para campos de confirmação/indicadores.
  - Categorização de receitas (`Holerite`, `CNPJ`, `Freelancer`) na aba `Notas`.
- **Cálculo Automático:**
  - Soma automática dos valores bancários na aba `Informes` por meio da função `SUM`.
- **Base de Referência:**
  - Lista centralizada de instituições financeiras na aba `Tabelas` para apoiar a padronização dos nomes dos bancos.
