# GetNextLineAlpr
A function that reads a certain amount of bytes and returns the first line from the readed bytes. This project is about file manipulation.

unistd -> write

search_and_replace

1. 1. string içinde döngü aç
2. 1. string içinde 1. charı görene kadar içeride ilerle ve charları yazdır
3. 1. string içinde 1. charı  görürsen 3. charla değiştir
4. sona newline ekle

----------------------------------------------------------
camel to snake

1. string içinde döngü aç
2. döngüde büyük harf tespit edilirse büyük harfi küçük yap
3. ekrana _ yazdır
4. ekrana harfi yazdır
5. repeat

-----------------------------------------------------------
snake to camel

1. string içinde döngü aç
2. döngüde _ işareti tespit edilirse önce döngüyü 1 sonraki indexe taşı "i++"
3. sonraki indexi uppercase yap
4. sonra indexi yazdır
5. repeat

------------------------------------------------------------

do_op -> stdlib for atoi , stdio for printf

------------------------------------------------------------

atoi

1. boşlukları ve ascii 9 - 13 arasını atla
2. - görürsen sign değerini - ile çarp
3. sonrasında - ve + değeri görüldüyse 1 atla (1 defa)
4. index 0 - 9 arası olduğu surece res = res * 10 + (str - '0')
5. sign * res döndür

basit vers

1. n = 0
2. string içinde döngü
3. n *= 10
4. n += *str - '0'
------------------------------------------------------------

strcmp

iki stringin içindede i döngüsü başlat, eğer charlar uyuşmazsa 1. - 2. şeklinde char farkını döndür

------------------------------------------------------------

strcspn

1. stringin içinde 2. stringin herhangi bir elemanını görene kadar karakter sayısını say
2. sayıyı döndür

------------------------------------------------------------

strdup

1. stringin uzunluğunu bul
2. length + 1 kadar memo allocla
3. stringi alloclanan memoya yazdır
4. sonuna null

-------------------------------------------------------------

strpbrk

1. stringin içinde döngü aç
2. içeride 2. string içinde bulunan herhandi bir chara rastlanana kadar devam et
3. rastlanırsa o charı  gösteren bir pointer döndür

------------------------------------------------------------

strrev

1. stringin uzunluğunu bul
2. stringin yarısına kadar döngü başlat
3. döngüden geçen her karakteri stringin simetrik karakteri ile swapla

-----------------------------------------------------------

strspn

string içinde döngü aç

-----------------------------------------------------------

inter

1. arg kontrol
2. string içinde döngü
3. 	inter fonksiyonu -> ?????

-----------------------------------------------------------

is power of 2

1. 0  sa 0 döndür
2. while n % 2 - n /= 2;
3. (n == 1) ? 1 : 0

-----------------------------------------------------------

last_word

1. stringin sonuna gel
2. sondaki boşlık ve tabları atla
3. sonra boşluk veya tab görene kadar stringde geri gel
4. daha sonra mevcut konumdan kelime sonuna kadar yazdır

----------------------------------------------------------

max

1. arrayın ilk elamanını max tanımla
2. dizi çinde döngü başlat
3. döngüde maxtan yüksek değere rastlanırsa yeni maxı o değer tanımla

---------------------------------------------------------

print bits

1.  8 den 0 a döngü başlat
2.  her seferinde i kadar sağa kaydır ve 1 ile ve sini al (yani i. bit 1 ise 1 değilse 0 döner) ve char 0 ekle ki yazdırabilelim

---------------------------------------------------------

reverse bits

1. 8 den 0 a döngğ
2.  ??????????????

---------------------------------------------------------

swap bits

return(octet >> 4 | octet << 4)

---------------------------------------------------------

wdmatch

1. arg cont
2. 2. string içinde döngü aç
3. if (argv[2][j++] == argv[1][i]) i++; -> yani 1. stringi 2. inin içinde 	arayacak fakat karakter karakter her karakter bulduğunda 	sonrakine geçcek
4. eğer 1. stringin sonuna gelinmişse yani 1. stringteki tüm karakterler
	2. inin içinde sırasıyla buşunuyorsa ekrana yazdır
 
---------------------------------------------------------

add prime sum

1. asal kontrolü yapan bir fonksiyon yaz
2. önce girilen argümanı atoi ile inte döndür
3. sonra o değere kadar döngü başlat, rastlanan her prime sayıyı topla

---------------------------------------------------------

atoi base

---------------------------------------------------------

range

1. len değerini bul -> end - start -> mutlağını al -> 0 dan küçükse * (-1)
2. res diye bir array aç ve mallocla len * int kadar yer aç
3. 0 dan lene döngü başlat 
4. eğer start < end
	a. resin içine startı her döngüde 1 artacak şekilde at
   değilse
	b. resin içine startı her döngüde 1 azalacak şekilde at

rrange

range ile aynısı sadece startla end yer değişsin (ters)

----------------------------------------------------------

lcm

1. arg cont
2. a ve b içerisinden büyük olanı n değişkenine tanımla
3. sonsuz döngü başlat, eğer n % a ve n % b aynanda 0 verirse n i döndür
4. her seferde n i 1 arttır

----------------------------------------------------------

paramsum

1. putnbr fonksiyonu yaz
2. putnbr ile argc - 1 i ekrana yazdır

---------------------------------------------------------

print hex (n)

1.hexdigits adında 0 dan 9 a ve a dan f e kadar tüm karakterleri içeren
char dizisi aç
2. n 16 dan büyükse n / 16 nın recurisive sini çalıştır
3. en sonrda write(1, &hexdigits[n % 16], 1);

---------------------------------------------------------

str capitaliser

stringdeki kelimelerin ilk harfini büyük sonraki tüm harflerü küçük yap

rstr

ilk yerine son harfleri büyük yap gerisi aynı

----------------------------------------------------------

flood_fill


void	fill(char **tab, t_point size, t_point cur, char to_fill)
{
	if (cur.y < 0 || cur.y >= size.y || cur.x < 0 || cur.x >= size.x
		|| tab[cur.y][cur.x] != to_fill)
		return;

	tab[cur.y][cur.x] = 'F';

	fill(tab, size, (t_point){cur.x - 1, cur.y}, to_fill);
	fill(tab, size, (t_point){cur.x + 1, cur.y}, to_fill); -
	fill(tab, size, (t_point){cur.x, cur.y - 1}, to_fill);
	fill(tab, size, (t_point){cur.x, cur.y + 1}, to_fill);
}

--------------------------------------------------------------

fprime

1. atoi ile argümanı inte dönüştür (n)
2. 1 se 1 yazdırsın
3. i den n e kadar döngü
4. eğer n % i = 0
	a. yazdır ve eğer n = i döngüyü kır
	b. * yaz
	c. n /= i;
	d. i = 1

yani döngüde 0 dan n e kadar sayıları bölenmi diye kontrol ediyoruz
bulduğumuzda ekrana yazdırıp böldükten sonra aynı şekilde ekrana yazdırıyoruz

-------------------------------------------------------------

ft_list_foreach

1. heada pointer at
2. listenin sonuna kadar döngğü aç
3. parametre olarag girilen fonksiyona tüm dataları sok
	(*f)(parametre) şeklinde






