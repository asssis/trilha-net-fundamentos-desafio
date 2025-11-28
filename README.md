# 🚗 Sistema de Estacionamento — Desafio DIO .NET  
www.dio.me => Assis Melhorias
 ![2025-11-27-21-29-41](https://github.com/user-attachments/assets/2a04eab6-b5cc-44c2-a2ab-2451fb4f071c)

## 📌 Sobre o desafio
Este projeto faz parte da **Trilha .NET — Fundamentos** da Digital Innovation One (DIO).  
O objetivo é construir um sistema simples de estacionamento capaz de:

- Cadastrar veículos  
- Remover veículos (calculando o valor devido)  
- Listar veículos  
- Encerrar o programa  

Para isso, o desafio original exige a criação da classe **Estacionamento**, contendo:

- `precoInicial : decimal`  
- `precoPorHora : decimal`  
- `veiculos : List<string>`  

E os métodos:

- `AdicionarVeiculo()`  
- `RemoverVeiculo()`  
- `ListarVeiculos()`

Além de um menu interativo com as opções:

1. Cadastrar veículo  
2. Remover veículo  
3. Listar veículos  
4. Encerrar  

---

# 🛠 Melhorias adicionadas (minhas contribuições)

Além de cumprir todos os requisitos do desafio, implementei diversas melhorias que tornam o sistema mais funcional, visualmente agradável e próximo de um software real.

## ✨ **1. Menu Interativo com Navegação pelas Setas**
- Interface amigável  
- Destaque visual da opção selecionada  
- Navegação com **↑** e **↓**

## ✨ **2. Cabeçalho Fixo “SISTEMA DE ESTACIONAMENTO”**
Sempre exibido **antes de qualquer entrada** do usuário para garantir identidade visual e organização.

## ✨ **3. Persistência de Dados via JSON**
Tudo é salvo em `data.json` automaticamente:
- Veículos estacionados  
- Histórico de remoções  
- Preço inicial  
- Preço por hora  

E recarregado automaticamente ao iniciar o programa.

## ✨ **4. Novo Menu: Configurar Preços**
Agora o usuário pode alterar os valores a qualquer momento através do menu:
```
5. Configurar preços
```

## ✨ **5. Validação Real das Placas**
Suporte para:
- `ABC1234` (modelo antigo)  
- `ABC1D23` (Mercosul)  

Mensagens claras para erros.

## ✨ **6. Histórico Completo de Remoções**
Cada saída registra:
- Placa  
- Entrada  
- Saída  
- Horas  
- Valor pago  

Além disso:
- Exibe total faturado  
- Exibe vagas ocupadas  

## ✨ **7. Cálculo Automático das Horas**
Se o usuário apenas apertar ENTER ao remover um veículo:
- O sistema calcula automaticamente o tempo de permanência.

## ✨ **8. Formatação PT-BR**
Todos os valores aparecem assim:
```
R$ 12,50
```

## ✨ **9. Código Organizado em 3 Arquivos**
- `Program.cs`
- `MenuUI.cs`
- `Models/Estacionamento.cs`

Organização semelhante a um projeto profissional.

## ✨ **10. Interface Colorida e Mais Intuitiva**
- Mensagens em verde (sucesso)
- Vermelho (erro)
- Amarelo (aviso)
- Azul/ciano (títulos)

---

# 📂 Estrutura do Projeto

```
/DesafioFundamentos
 ├── Program.cs
 ├── MenuUI.cs
 ├── Models/
 │    └── Estacionamento.cs
 ├── data.json   (gerado automaticamente)
 └── README.md
```

---

# ▶ Como executar

No terminal:

```bash
dotnet run
```

O arquivo `data.json` será criado automaticamente na primeira execução.

---

# 📘 Funcionalidades Implementadas

### ✔ 1 — Cadastrar veículo  
Inclui validação de placa e persistência automática.

### ✔ 2 — Remover veículo  
Calcula valor, permite horas manuais ou automáticas e salva no histórico.

### ✔ 3 — Listar veículos  
Lista todos os veículos presentes no estacionamento.

### ✔ 4 — Mostrar histórico  
Exibe todas as saídas, incluindo horas e valor pago.

### ✔ 5 — Configurar preços  
Permite editar o preço inicial e o preço por hora.

### ✔ 6 — Encerrar  
Finaliza o programa.

---

# 🎨 Demonstração visual do menu

```
╔══════════════════════════════════════╗
║        SISTEMA DE ESTACIONAMENTO     ║
╚══════════════════════════════════════╝

> Cadastrar veículo
  Remover veículo
  Listar veículos
  Mostrar histórico
  Configurar preços
  Encerrar
```

---

# 🧾 Conclusão

Este projeto atende totalmente ao desafio original, mas foi expandido para incluir:

- Persistência real de dados  
- Tela mais amigável e profissional  
- Validações extensivas  
- Histórico detalhado  
- Configurações dinâmicas  

O resultado é um sistema robusto, organizado e muito superior ao escopo inicial do desafio — refletindo boas práticas de desenvolvimento.
