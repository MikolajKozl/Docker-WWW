# Website (Docker Compose) — WordPress + Nginx + MariaDB

Osobista strona postawiona na Docker Compose,
hostowana na AWS EC2 za Cloudflare.

## Architektura
Internet → Cloudflare (SSL) → Nginx → WordPress (PHP-FPM) → MariaDB

## Stack technologiczny
- **Nginx** — reverse proxy
- **WordPress 6.9** — CMS
- **MariaDB 10.11** — baza danych
- **Docker Compose** — orkiestracja kontenerów
- **Cloudflare** — SSL, CDN, ochrona DDoS
- **AWS EC2** — hosting (t2.micro, Free Tier)

## Uruchomienie lokalne

```bash
git clone https://github.com/TwójNick/portfolio
cd portfolio
cp .env.example .env
# uzupełnij hasła w .env
docker compose up -d
```

## Struktura projektu
```
├── docker-compose.yml
├── nginx-conf/
│   └── nginx.conf
├── .env.example
└── README.md
```
