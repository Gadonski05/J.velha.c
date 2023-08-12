# J.velha.c
Projeto básico do jogo da velha.

#include <stdio.h>

typedef struct {
    char nome[100];
    int idade;
    float salario;
    int anos;
    char cargo[50];
} funcionario;

void cadastra(funcionario *f) {
    for (int i = 1; i < 3; i++) {
        printf("\n----funcionario %i----\n", i);
        printf("Digite o nome: ");
        scanf(" %[^\n]", f[i].nome);
        printf("Digite a idade: ");
        scanf("%i", &f[i].idade);
        printf("Digite o salario: ");
        scanf("%f", &f[i].salario);
        printf("Digite quantos anos de empresa: ");
        scanf("%i", &f[i].anos);
        printf("Digite o cargo: ");
        scanf(" %[^\n]", f[i].cargo);
    }
}

void imprime(funcionario *f) {
    for (int i = 1; i < 3; i++) {
        printf("\n----Dados do funcionario %i----\n", i);
        printf("Nome: %s\n", f[i].nome);
        printf("Idade: %i\n", f[i].idade);
        printf("Salario: %.2f\n", f[i].salario);
        printf("Anos: %i\n", f[i].anos);
        printf("Cargo: %s\n", f[i].cargo);
    }
}

void mediaidade(funcionario *f) {
    int somaidades = 0;
    for (int i = 1; i < 3; i++) {
        somaidades += f[i].idade;
    }
    float media = (float) somaidades / 2;
    printf("\nIdade media: %.2f\n", media);
}

int main(void) {
    funcionario f[2];
    
    cadastra(f);
    imprime(f);
    mediaidade(f);
    
    return 0;
}

