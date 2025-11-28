#include <stdio.h>

int main()
{
	int n,i;
	printf("Nhap so phan tu cua mang: ");
	scanf("%d", &n);
	int* mang = (int*)malloc(n * sizeof(int));
	for (i = 0; i < n; i++)
	{
		printf("Nhap phan tu thu %d: ", i + 1);
		scanf("%d", &mang[i]);
	}
	float tong = 0;
	int count = 0;
	for (i = 0; i < n; i++)
	{
		if (mang[i] % 3 == 0)
		{
			tong += mang[i];
			count++;
		}
	}
	if (count == 0)
	{
		float Tb = tong / count;
		printf("Trung binh cong cac so chia het cho 3 la: %.2f\n", Tb);
	}
	else
	{
		printf("Khong co so nao chia het cho 3 trong mang.\n");
	}
	return 0;
		

}
