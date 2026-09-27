# Tugas-Asistensi
    #include <stdio.h>

    int main() {
    char nama[50];
    char fav_drink[50];
    int umur;
   
    char id[50];
    char temp_part1[20];
    char temp_part2[20];
    printf("Masukkan Nama          :");
    scanf("%[^\n]", nama);

    printf("Masukkan Minuman Favorit : ");
    scanf(" %[^\n]", fav_drink);

    printf("Masukkan Umur          : ");
    scanf("%d", &umur);
   
   //ID Generator
   
    char inisial_nama = nama[0];
   
    int op_matematika1 = 2026 - umur;
    
    char inisial_drink = fav_drink[0];
   
    int ascii_drink;
    
    if (inisial_drink >= 'a' && inisial_drink <= 'z') {
        ascii_drink = (inisial_drink - 32) + inisial_drink; // Ubah ke kapital + asli
    } else if (inisial_drink >= 'A' && inisial_drink <= 'Z') {
        ascii_drink = (inisial_drink + 32) + inisial_drink; // ubah ke non-kapital + asli
    } else {
        ascii_drink = inisial_drink * 2;
    }
    
    int len_nama = 0;
    while (nama[len_nama] != '\0') {
        len_nama++; 
    }
    char akhiran_nama = nama[len_nama - 1];
    
    sprintf(temp_part1, "%c%d%d", inisial_nama, op_matematika1, umur);
    sprintf(temp_part2, "%d%c", ascii_drink, akhiran_nama);
    sprintf(id, "%s%s", temp_part1, temp_part2);
    
    printf("\n-----------------------------------\n");
    printf("| ID             : %-15s |\n", id);
    printf("| Name           : %-15s |\n", nama);
    printf("| Minuman Favorit: %-15s |\n", fav_drink);
    printf("-----------------------------------\n");
    return 0;
    }
