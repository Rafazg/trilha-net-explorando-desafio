# DIO - Trilha .NET - Explorando a linguagem C#
www.dio.me

## Desafio de projeto
Para este desafio, você precisará usar seus conhecimentos adquiridos no módulo de explorando a linguagem C#, da trilha .NET da DIO.

## Contexto
Você foi contratado para construir um sistema de hospedagem, que será usado para realizar uma reserva em um hotel. Você precisará usar a classe Pessoa, que representa o hóspede, a classe Suíte, e a classe Reserva, que fará um relacionamento entre ambos.

O seu programa deverá cálcular corretamente os valores dos métodos da classe Reserva, que precisará trazer a quantidade de hóspedes e o valor da diária, concedendo um desconto de 10% para caso a reserva seja para um período maior que 10 dias.

## Regras e validações
1. Não deve ser possível realizar uma reserva de uma suíte com capacidade menor do que a quantidade de hóspedes. Exemplo: Se é uma suíte capaz de hospedar 2 pessoas, então ao passar 3 hóspedes deverá retornar uma exception.
2. O método ObterQuantidadeHospedes da classe Reserva deverá retornar a quantidade total de hóspedes, enquanto que o método CalcularValorDiaria deverá retornar o valor da diária (Dias reservados x valor da diária).
3. Caso seja feita uma reserva igual ou maior que 10 dias, deverá ser concedido um desconto de 10% no valor da diária.


![Diagrama de classe estacionamento](diagrama_classe_hotel.png)

## Solução

### 1. Verificação de Capacidade
- **Método:** `CadastrarHospedes`
- **Solução:** Verifica se o número de hóspedes não excede a capacidade da suíte. Lança uma exceção se exceder.

### 2. Cadastro da Suíte
- **Método:** `CadastrarSuite`
- **Solução:** Atribui a suíte à reserva.

### 3. Quantidade de Hóspedes
- **Método:** `ObterQuantidadeHospedes`
- **Solução:** Retorna o número de hóspedes na reserva.

### 4. Cálculo do Valor da Diária
- **Método:** `CalcularValorDiaria`
- **Solução:** Calcula o valor da diária e aplica um desconto de 10% se os dias reservados forem 10 ou mais.

### 5. Tratamento de Exceções
![Tratamento de Exceções](diagrama_classe_hotel.png)
- **Uso:** Em torno da chamada ao método `CadastrarHospedes`.
- **Solução:** Usa `try-catch` para capturar e exibir erros relacionados à capacidade da suíte.