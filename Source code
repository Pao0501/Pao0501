#include <stdio.h>


void win(int player, int winner, int pos[])
{
	// Print the board
	printf("\n");
	printf("%c|%c|%c\n", pos[0], pos[1], pos[2]);
	printf("-+-+-\n");
	printf("%c|%c|%c\n", pos[3], pos[4], pos[5]);
	printf("-+-+-\n");
	printf("%c|%c|%c\n", pos[6], pos[7], pos[8]);
	if (winner)
	{
		printf("Winner is player %d\n", player);
	}
	else
	{
		printf("Match is a draw\n");
	}
}


// Main code
int main()
{
	// Declare Variables 
	int winner = 0, count = 0;
	int pos[9], index, sign, player, flag, s, k, j;


	// Assign empty spaces
	for (s = 0; s < 9; s++)
	{
		pos[s] = '  ';


	}


	while (count < 9 && winner != 1)
	{
		flag = 0;

		// Print the board
		printf("\n");
		printf("%c|%c|%c\n", pos[0], pos[1], pos[2]);
		printf("-+-+-\n");
		printf("%c|%c|%c\n", pos[3], pos[4], pos[5]);
		printf("-+-+-\n");
		printf("%c|%c|%c\n",  pos[6], pos[7], pos[8]);


		if (count % 2 == 0)
		{
			sign = 'X';
			player = 1;

		}

		else
		{
			sign = 'O';
			player = 2;

		}
		// Player select a move 
		printf("Seclect a space player%d(1-9): ", player);
		scanf_s("%d", &index);

		// Check player input 
		if (index < 1 || index > 9)
		{

			printf("Allowed index is 1 to 9\n");
			continue;
		}

		if (pos[index - 1] == 'X' || pos[index - 1] == 'O')
		{
			printf("Allowed index is 1 to 9");
			continue;
		}

		pos[index - 1] = sign;
		count++;

		// Check if current player has 1
		for (s = 0; s < 9; s++)
		{
			if (s % 3 == 0)
				flag = 0;

			if (pos[s] == sign)
				flag++;
			if (flag == 3)
			{
				winner = 1;
				win(player, winner, pos);

			}

		}

		// Check for winner
		flag = 0;

		for (s = 0; s < 3; s++)
		{
			for (k = s; k <= s + 6; k += 3)
			{
				if (pos[k] == sign)
					flag++;
			}

			if (flag == 3)
			{
				winner = 1;
				win(player, winner, pos);

			}
		}

		// Check diagnol Winner 
		flag = 0;
		if ((pos[0] == sign && pos[4] == sign && pos[8] == sign) || (pos[2] == sign && pos[4] == sign && pos[6] == sign))
		{
			winner = 1;
			win(player, winner, pos);

		}
	}

}
