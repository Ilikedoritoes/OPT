#define _CRT_SECURE_NO_WARNINGS
#include <stdlib.h>
#include <stdio.h>

int OPT(int num1, char op, int num2)
{
	if (op == '+')
		return num1 + num2;
	if (op == '%')
		return num1 % num2;
	if (op == '-')
		return num1 - num2;
	if (op == '/')
		return num1 / num2;
	if (op == '*')
		return num1 * num2;
	if ((op != '+') && (op != '%') && (op != '-') && (op != '/') && (op != '*'))
		printf("ERROR");
}

void main()
{
	int num1, num2, answer;
	char op;
	printf("gimme 2 numbers pls\n");
	scanf("%d %c %d", &num1, &op, &num2);

	answer = OPT(num1, op, num2);
	printf("%d", answer);

}
