  
/\*1  
Ispišite ime, prezime, patronus svih likova koji imaju patronusa i on je poznat.  
\*/  
select fname,lname,patronus  
from characters  
where not patronus  \= 'Unknown' and patronus is not null;

/\*2.Ispišite prezime likova čije prezime se završava slovom 'e'.  
\*/  
select lname  
from characters  
where lname like '\_%e';

/\*3.Izračunajte ukupne godine svih likova i ispišite to na ekran.\*/  
select sum(age) from characters;

/\*4.Ispišite ime, prezime i godine likova po opadajućem redosledu njihovih godina.\*/  
select fname,lname,age from characters  
order by age desc;

/\*5.Ispišite ime likova i godine onih čije godine su u rasponu od 50 do 100 godina.\*/  
select fname,age from characters  
where age between 50 and 100;

/\*6.Ispišite godine svih likova tako da među njima nema onih sa istim godinama.\*/  
select distinct age from characters;

/\*7.Ispišite sve informacije o likovima čiji je faculty \= Gryffindor i čije su godine preko 30\*/  
select \* from characters  
where faculty \= 'Gryffindor' and age \> 30;

/\*8.Ispišite imena prva tri fakulteta iz tabele tako da se fakulteti ne ponavljaju\*/  
select faculty from characters  
group by faculty  
limit 3;

/\*9.Ispišite imena likova čije ime počinje sa 'N' i ima 5 slova, ili čije ime počinje sa 'L'.\*/  
select fname from characters  
where fname like 'N\_\_\_\_' or fname like 'L%';

/\*10.Izračunajte prosečne godine svih likova.\*/

select avg(age) from characters;

/\*11.Obrišite lika sa ID \= 11.\*/  
delete from characters  
where char\_id=11;

/\*12.Ispišite prezime svih likova koja sadrže slovo 'a'.\*/  
select lname from characters  
where lname like '%a%';

/\*13.Koristite pseudonim da privremeno zamenite naziv kolone fname u Half-Blood Prince za stvarnog princa-polukrvnog.\*/  
select fname as 'Half-Blood Prince' from characters;

/\*14.Ispišite id i imena svih patronusa po abecednom redu, pod uslovom da su poznati.\*/  
select char\_id, patronus from characters  
where not patronus  \= 'Unknown' and patronus is not null  
order by patronus asc;

/\*15.Koristite operator IN, ispišite ime i prezime likova čije je prezime Crabbe, Granger ili Diggory.\*/  
select fname, lname from characters  
where lname in('Crabbe','Granger','Diggory');

/\*16.Ispišite minimalne godine likova.\*/  
select min(age) from characters;

/\*17.Koristite operator UNION, ispišite imena iz tabele characters i naslove knjiga iz tabele library.\*/  
select fname from characters  
union   
select book\_name from library;

/\*18.Koristite operator HAVING, izračunajte broj likova po svakom fakultetu, ostavljajući samo one fakultete gde je broj studenata veći od 1.\*/  
select count(char\_id), faculty from characters  
group by faculty  
having count(char\_id ) \> 1;

/\*NAPREDNI NIVO\*/  
/\*1.Ispišite ime, prezime likova i naziv knjige koja im pripada.\*/  
select   
    c.fname as 'Ime',  
    c.lname as 'Prezime',  
    l.book\_name as 'Naziv knjige'  
from characters c  
join library l on c.char\_id \= l.char\_id;

/\*2.Ispišite ime, prezime likova i naziv knjige, bez obzira na to da li imaju knjige ili ne\*/  
select   
    c.fname as 'Ime',  
    c.lname as 'Prezime',  
    l.book\_name as 'Naziv knjige'  
from characters c  
left join library l on c.char\_id \= l.char\_id;

/\*3.Ispišite naziv knjige i ime patronusa, bez obzira na to da li je informacija o vlasniku knjige u tabeli ili ne.\*/  
select   
	l.book\_name as 'Naziv knjige',  
    c.patronus as 'Patronus'  
from characters c  
left join library l on c.char\_id \= l.char\_id;

/\*4.Ispišite ime, prezime, godine likova i naziv knjige koja im pripada, pod uslovom da su svi vlasnici knjiga stariji od 15 godina.\*/  
select   
    c.fname as 'Ime',  
    c.lname as 'Prezime',  
    c.age as "Age",  
    l.book\_name as 'Naziv knjige'  
from characters c  
left join library l on c.char\_id \= l.char\_id  
where age \> 15;

/\*5.Ispišite ime lika, naziv knjige, datum izdavanja i datum završetka, pod uslovom da je mlađi od 15 godina i njegov patronus nije poznat\*/  
select   
    c.fname as 'Ime',  
    l.book\_name as 'Naziv knjige',  
    l.start\_date as "Datum izdavanja",  
    l.end\_date as "Datum zavrsetka"  
from characters c  
left join library l on c.char\_id \= l.char\_id  
where age \< 15 and patronus \= 'Unknown';

/\*6.Koristite ugnježđeni upit za broj knjiga čiji je end\_date veći od end\_date kod Hermione.\*/

select COUNT(\*) as 'Broj knjiga'  
from library  
where end\_date \> (  
    select end\_date  
    from library l  
    join characters c on l.char\_id \= c.char\_id  
    where c.fname \= 'Hermione'  
);  
/\*7.Pomoću ugnježđenog upita ispišite imena svih patronusa čiji su vlasnici stariji od lika čiji je patronus Unknown.\*/  
select patronus as 'Patronus'  
from characters  
where age \> (  
select age from characters  
where patronus \= 'Unknown'  
);  
