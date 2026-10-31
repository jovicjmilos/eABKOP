# Zajednički rad

1. Pre početka preuzmite najnoviji `main` i napravite svoju granu, npr. `milos/opis-izmene` ili `perica/opis-izmene`.
2. Pošaljite granu na GitHub i otvorite pull request prema `main`.
3. Sačekajte zelen rezultat `Repository checks` i pregled drugog saradnika. Svaka nova izmena u pull requestu ponavlja proveru.
4. Ako se `main` promenio, ažurirajte svoju granu i rešite eventualne konflikte pre spajanja. Ne koristite prisilno prepisivanje zajedničke grane.

## Šta se trenutno proverava

Workflow `.github/workflows/pr-checks.yml` proverava ostatke Git konflikata u tekstualnim datotekama i sintaksu JSON datoteka. Pokreće se za svaki pull request, za slanje u `main` i ručno kroz Actions. Ne objavljuje aplikaciju i ne koristi poslovnu bazu ili tajne.

Repozitorijum još nema kod aplikacije. Kada bude dodat, workflow treba proširiti stvarnim proverama projekta: testovima, proverom tipova/lintom i izgradnjom prema njegovim postojećim komandama. Zelen rezultat sada nije potvrda ispravnosti aplikacije.

## Zaštita glavne grane

Vlasnik repozitorijuma treba u Settings → Rules → Rulesets da zaštiti `main`: zahtevati pull request, najmanje jedno odobrenje drugog saradnika, uspešan `Repository checks`, ažurnu granu pre spajanja i blokirati force push i brisanje grane. Provere bez ovog pravila same ne sprečavaju spajanje ili direktno slanje na `main`.

Ne dodavati lozinke, tokene, stvarne poslovne podatke ili izvoze baze u ovaj javni repozitorijum.
