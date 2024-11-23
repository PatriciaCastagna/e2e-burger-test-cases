# e2e-burger-test-cases
A collection of test cases for the E2E Burger platform, focusing on order management, menu organization, and workflow between staff and kitchen. It validates user interactions on both web and mobile platforms this work available for business E2E training.

## Methodology
The test cases in this repository follow the **Behavior-Driven Development (BDD)** methodology using the **Given, When, Then** structure to describe each scenario. This approach helps in clearly defining the behavior of the application from a user’s perspective.



# Test Cases for Frontend Registration Validation

## Table of Contents
1. [English Version](#english-version)
2. [Versão em Português](#versão-em-português)

---

## English Version

### Scenario 1: Registration failure due to invalid email
| **Step**         | **Action**                                             |
|-------------------|-------------------------------------------------------|
| **Given**         | The user accesses the registration page.             |
| **And**           | Fills in the mandatory fields with:                  |
|                   | - Full name: João Silva                              |
|                   | - Email: joaoemail.com (invalid)                     |
|                   | - Password: Senha@123                                |
|                   | - Password confirmation: Senha@123                   |
| **When**          | The user clicks the "Register" button.               |
| **Then**          | The registration must not be completed.              |
| **And**           | A toast message appears: "Please enter a valid email address." |

---

### Scenario 2: Registration failure due to duplicate email
| **Step**         | **Action**                                             |
|-------------------|-------------------------------------------------------|
| **Given**         | The user accesses the registration page.             |
| **And**           | Fills in the mandatory fields with:                  |
|                   | - Full name: João Silva                              |
|                   | - Email: joao@email.com (already registered)         |
|                   | - Password: Senha@123                                |
|                   | - Password confirmation: Senha@123                   |
| **When**          | The user clicks the "Register" button.               |
| **Then**          | The registration must not be completed.              |
| **And**           | A toast message appears: "Error during registration. Please try again or use a different email address!" |

---

### Scenario 3: Registration failure due to weak password
| **Step**         | **Action**                                             |
|-------------------|-------------------------------------------------------|
| **Given**         | The user accesses the registration page.             |
| **And**           | Fills in the mandatory fields with:                  |
|                   | - Full name: João Silva                              |
|                   | - Email: joao@email.com                              |
|                   | - Password: senha123 (does not meet validation criteria) |
|                   | - Password confirmation: senha123                    |
| **When**          | The user clicks the "Register" button.               |
| **Then**          | The registration must not be completed.              |
| **And**           | An error message appears: "The password must be between 8 and 12 characters long and include at least one uppercase letter, one number, and one special character." |

---

### Scenario 4: Registration failure due to mismatched passwords
| **Step**         | **Action**                                             |
|-------------------|-------------------------------------------------------|
| **Given**         | The user accesses the registration page.             |
| **And**           | Fills in the mandatory fields with:                  |
|                   | - Full name: João Silva                              |
|                   | - Email: joao@email.com                              |
|                   | - Password: Senha@123                                |
|                   | - Password confirmation: Senha@321                   |
| **When**          | The user clicks the "Register" button.               |
| **Then**          | The registration must not be completed.              |
| **And**           | An error message appears: "Passwords do not match."  |

---

## Versão em Português

### Cenário 1: Falha no cadastro por e-mail inválido
| **Etapa**         | **Ação**                                              |
|-------------------|-------------------------------------------------------|
| **Dado que**      | O usuário acessa a página de cadastro.               |
| **E**             | Preenche os campos obrigatórios com:                 |
|                   | - Nome completo: João Silva                          |
|                   | - E-mail: joaoemail.com (inválido)                   |
|                   | - Senha: Senha@123                                   |
|                   | - Confirmação de senha: Senha@123                    |
| **Quando**        | O usuário clica no botão "Cadastrar".                |
| **Então**         | O cadastro não deve ser realizado.                   |
| **E**             | Um toast deve ser exibido: "Por favor, insira um e-mail válido." |

---

### Cenário 2: Falha no cadastro por e-mail duplicado
| **Etapa**         | **Ação**                                              |
|-------------------|-------------------------------------------------------|
| **Dado que**      | O usuário acessa a página de cadastro.               |
| **E**             | Preenche os campos obrigatórios com:                 |
|                   | - Nome completo: João Silva                          |
|                   | - E-mail: joao@email.com (já cadastrado)             |
|                   | - Senha: Senha@123                                   |
|                   | - Confirmação de senha: Senha@123                    |
| **Quando**        | O usuário clica no botão "Cadastrar".                |
| **Então**         | O cadastro não deve ser realizado.                   |
| **E**             | Um toast deve ser exibido: "Erro ao realizar cadastro. Tente novamente ou verifique um outro e-mail!" |

---

### Cenário 3: Falha no cadastro por senha fraca
| **Etapa**         | **Ação**                                              |
|-------------------|-------------------------------------------------------|
| **Dado que**      | O usuário acessa a página de cadastro.               |
| **E**             | Preenche os campos obrigatórios com:                 |
|                   | - Nome completo: João Silva                          |
|                   | - E-mail: joao@email.com                             |
|                   | - Senha: senha123 (não atende aos critérios de validação) |
|                   | - Confirmação de senha: senha123                     |
| **Quando**        | O usuário clica no botão "Cadastrar".                |
| **Então**         | O cadastro não deve ser realizado.                   |
| **E**             | Uma mensagem de erro deve ser exibida: "A senha deve ter entre 8 e 12 caracteres, incluir ao menos uma letra maiúscula, um número e um caractere especial." |

---

### Cenário 4: Falha no cadastro por senhas diferentes
| **Etapa**         | **Ação**                                              |
|-------------------|-------------------------------------------------------|
| **Dado que**      | O usuário acessa a página de cadastro.               |
| **E**             | Preenche os campos obrigatórios com:                 |
|                   | - Nome completo: João Silva                          |
|                   | - E-mail: joao@email.com                             |
|                   | - Senha: Senha@123                                   |
|                   | - Confirmação de senha: Senha@321                    |
| **Quando**        | O usuário clica no botão "Cadastrar".                |
| **Então**         | O cadastro não deve ser realizado.                   |
| **E**             | Uma mensagem de erro deve ser exibida: "As senhas não coincidem." |

