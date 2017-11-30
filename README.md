# Program
sucessor
.data

mensagem:	.asciiz "Digite um numero: "
mensagem2: 	.asciiz "sucessor: "
num:	.word 1
rsp:	.word 1
	.text
main:	addi $v0, $zero, 4
	la $a0, mensagem
	syscall
	addi $v0, $zero, 5
	syscall
	sw $v0, num
	addi $s1, $v0, 1
	sw $s1, rsp
	addi $v0, $zero, 4
	la $a0, mensagem2
	syscall
	addi $v0, $zero, 1
	add $a0, $s1, $zero
	syscall
	jr$ra
	
