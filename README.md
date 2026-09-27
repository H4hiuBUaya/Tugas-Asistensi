# Tugas-Asistensi
    #include <stdio.h>
    
    int main() {
    char nama[50];
    char fav_food[50];
    int umur;
   
    char id[50];
    char temp_part1[20];
    char temp_part2[20];
    printf("Masukkan Nama            : ");
    scanf("%[^\n]", nama);

    printf("Masukkan Makanan Favorit : ");
    scanf(" %[^\n]", fav_food);

    printf("Masukkan Umur            : ");
    scanf("%d", &umur);
   
   //ID Generator
   
    char inisial_nama = nama[0];
   
    int op_matematika1 = 2026 - umur;
   
    char inisial_food = fav_food[0];
    int ascii_food;
    if (inisial_food >= 'a' && inisial_food <= 'z') {
        ascii_food = (inisial_food - 32) + inisial_food^2; // Ubah ke kapital + asli
    } else if (inisial_food >= 'A' && inisial_food <= 'Z') {
        ascii_food = (inisial_food + 32) + inisial_food^2; // ubah ke non-kapital + asli
    } else {
        ascii_food = inisial_food * 2;
    }
    
    int len_nama = 0;
    while (nama[len_nama] != '\0') {
        len_nama++; 
    }
    char akhiran_nama = nama[len_nama - 1];
    
    sprintf(temp_part1, "%c%d%d", inisial_nama, op_matematika1, umur);
    sprintf(temp_part2, "%d%c", ascii_food, akhiran_nama);
    sprintf(id, "%s%s", temp_part1, temp_part2);
    
    printf("\n-----------------------------------\n");
    printf("| ID             : %-15s |\n", id);
    printf("| Name           : %-15s |\n", nama);
    printf("| Makanan Favorit: %-15s |\n", fav_food);
    printf("-----------------------------------\n");
    return 0;
    }
Hasil Running Program :
<img width="283" height="201" alt="image" src="https://github.com/user-attachments/assets/4a1c8317-d377-46fc-914e-13a4d4050cc1" />


