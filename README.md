graph TD
    %% Hlavní uzly
    A[Veřejná správa] --> B(Státní správa);
    A --> C(Samospráva);

    %% Rozdělení Státní správy
    B --> B1[Nejvyšší ústavní orgány];
    B --> B2[Ústřední správní úřady];
    B --> B3[Podřízené správní úřady];
    B --> B4[Nezávislé orgány a bezrozsudkové složky];
    B --> B5[Ostatní státem zřízené subjekty];

    %% Příklady Státní správy
    B1 --> B1a(Prezident, Parlament, Vláda);
    B2 --> B2a(Ministerstva - MF, MV, MZd);
    B3 --> B3a(Jiné ÚSÚ - ČSÚ, ÚOHS);
    B4 --> B4a(ČNB, NKÚ);
    B5 --> B5a(Lesy ČR, VZP);

    %% Rozdělení Samosprávy
    C --> C1[Územní Samospráva];
    C --> C2[Zájmová/Profesní Samospráva];

    %% Podčásti Územní Samosprávy
    C1 --> C1a[Kraje];
    C1 --> C1b[Obce];
    C1 --> C1c[Hl. město Praha];

    C1a --> C1a1(Krajský úřad, Zastupitelstvo);
    C1b --> C1b1(Obecní úřad, Zastupitelstvo);

    %% Podčásti Zájmové Samosprávy
    C2 --> C2a(Profesní komory);
    C2 --> C2b(Vysoké školy);

    %% Působnost (propojení)
    C1 --> D{Působnost};
    B --> D;

    D --> D1[Samostatná působnost];
    D --> D2[Přenesená působnost];

    %% Delegace Státní správy na ÚS
    B --> C1 |Delegace státní správy / Přenesená působnost|;

    %% Vysvětlení působnosti (Zjednodušené)
    D1 --> D1a(Vlastní správa ÚSC - např. místní poplatky);
    D2 --> D2a(Výkon státní správy - např. vydávání OP);

    %% Styl - pro lepší vizuální rozdělení (volitelné)
    classDef statni fill:#99ccff,stroke:#3366cc;
    classDef samosprava fill:#99ff99,stroke:#33cc33;
    class B,B1,B2,B3,B4,B5,B1a,B2a,B3a,B4a,B5a statni;
    class C,C1,C2,C1a,C1b,C1c,C2a,C2b,C1a1,C1b1 samosprava;

    %% Legenda (pro čitelnost)
    style A fill:#ffcc99,stroke:#ff6600
    style D fill:#cccccc,stroke:#666666

    click D "https://cs.wikipedia.org/wiki/Ve%C5%99ejn%C3%A1_spr%C3%A1va" _blank
