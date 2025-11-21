# Problematika relačních databází a rozdíl mezi SQL a NoSQL databázemi

## Relační databáze

Relační databáze je typ databáze, který ukládá a poskytuje přístup k datům organizovaným do předem definovaných tabulek (relací). Každá tabulka se skládá ze sloupců (atributů) a řádků (záznamů). Hlavní výhody relačních databází jsou:

1. **Strukturovanost a konzistence dat**: Data jsou uložena v tabulkách s pevně definovanými strukturami, což usnadňuje zajištění konzistence a integrity dat. To znamená, že data v tabulce musí splňovat určitá pravidla (například data v určitém sloupci musí být unikátní nebo nemohou být prázdná).

2. **Referenční integrita**: Relační databáze umožňuje definovat vztahy mezi tabulkami pomocí primárních a cizích klíčů. To zajišťuje, že vztahy mezi daty jsou platné a konzistentní, což je důležité pro udržení integrity dat.

3. **Transakční zpracování**: Relační databáze podporují transakce, které zajišťují, že více operací na databázi bude provedeno jako celek nebo vůbec. To je důležité pro zajištění integrity dat při složitých operacích, například při převodech peněz.

4. **Dotazování pomocí SQL**: Relační databáze používají jazyk SQL (Structured Query Language) pro dotazování a manipulaci s daty. SQL je standardizovaný a umožňuje složité dotazy na data.

## SQL databáze vs. NoSQL databáze

### SQL databáze
- **Struktura**: Data jsou ukládána do tabulek s pevnou strukturou (sloupce a řádky).
- **Schéma**: Vyžaduje předem definované schéma, které určuje strukturu dat (typy sloupců, povinná pole, apod.).
- **Transakce**: Podporuje ACID (Atomicity, Consistency, Isolation, Durability) vlastnosti, které zajišťují bezpečné a konzistentní zpracování transakcí.
- **Vhodnost**: Ideální pro aplikace, kde je důležitá konzistence a integrita dat, například bankovní systémy, účetní systémy, apod.
- **Příklady SQL databází**:
  - **MySQL**: Open-source relační databáze, široce používaná pro webové aplikace.
  - **PostgreSQL**: Pokročilá open-source relační databáze, známá pro svou robustní podporu datových typů a komplexních dotazů.
  - **Microsoft SQL Server**: Komerční relační databáze vyvinutá společností Microsoft, často používaná v podnikovém prostředí.
  - **Oracle Database**: Velmi rozšířená komerční databáze s podporou velkého množství funkcí a optimalizací pro různé typy aplikací.

### NoSQL databáze
- **Struktura**: Data mohou být ukládána v různých formátech, například dokumenty (JSON, XML), klíč-hodnota páry, grafy nebo sloupce. To umožňuje větší flexibilitu v ukládání různorodých dat.
- **Schéma**: Nevyžaduje pevně definované schéma, což umožňuje dynamicky měnit strukturu dat. To je užitečné pro aplikace s rychle se měnícími datovými potřebami.
- **Transakce**: Podporuje BASE (Basically Available, Soft state, Eventual consistency) model, který je méně striktní než ACID. To může být výhodné pro aplikace, které potřebují vysokou dostupnost a škálovatelnost.
- **Vhodnost**: Vhodné pro aplikace, které vyžadují rychlé čtení a zápis velkých objemů dat, například sociální sítě, analytické aplikace, IoT systémy, apod.
- **Příklady NoSQL databází**:
  - **MongoDB**: Dokumentová databáze, která ukládá data ve formátu JSON-like dokumentů, často používaná pro flexibilní datové struktury.
  - **Cassandra**: Distribuovaná sloupcová databáze, navržená pro škálovatelnost a vysokou dostupnost bez centrálního bodu selhání.
  - **Redis**: In-memory klíč-hodnota databáze, často používaná pro caching a real-time analytické aplikace.
  - **Neo4j**: Grafová databáze, která ukládá data ve formě uzlů a hran, což umožňuje efektivní reprezentaci a dotazování na složité vztahy mezi daty.

### Shrnutí
Relační databáze (SQL) jsou vhodné pro aplikace, kde je důležitá strukturovanost a konzistence dat, zatímco NoSQL databáze poskytují větší flexibilitu a škálovatelnost pro aplikace s různorodými datovými potřebami.
