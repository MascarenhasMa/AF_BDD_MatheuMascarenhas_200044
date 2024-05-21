# TesteQualidade-BDD

Feature: Sistema de Locação de Carros
  Para garantir uma experiência satisfatória para diferentes tipos de clientes
  Como uma empresa de locação de carros
  Eu quero que o sistema se adapte as locações dependendo das circunstâncias da reserva

  Scenario: Reserva antecipada de um carro de luxo com desconto
    Given um cliente deseja alugar um carro de luxo
    And o cliente realiza a reserva com antecedência de pelo menos uma semana
    When o cliente completa a reserva
    Then o sistema deve oferecer um desconto especial no valor total da locação

  Scenario: Locação de última hora de um carro utilitário
    Given um cliente necessita alugar um carro utilitário de última hora
    And o cliente não possui uma reserva prévia
    When o cliente solicita a locação
    Then o sistema deve encontrar um veículo disponível
    And o sistema deve processar a locação rapidamente
    And o sistema deve aplicar um custo adicional devido à demanda urgente
