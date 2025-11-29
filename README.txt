# Przetwarzanie rozproszone – projekt dwóch mikroserwisów (.NET 8)

Projekt przedstawia dwa niezależne mikroserwisy komunikujące się poprzez HTTP:

- ProductService – serwis produktów (port 5001)
- InventoryService – serwis magazynowy (port 5002)

InventoryService odpyta ProductService, aby zweryfikować produkt i zwrócić połączoną odpowiedź.

## Wymagania
- Windows 10/11
- .NET SDK 8.0
- Visual Studio 2022 z workloadem ASP.NET and web development

## Uruchamianie

### 1. ProductService (port 5001)
1. Otwórz projekt w Visual Studio
2. Wybierz profil uruchomienia: ProductService (Project)
3. Uruchom: Ctrl + F5
4. Test:
   http://localhost:5001/
   http://localhost:5001/products/1

### 2. InventoryService (port 5002)
1. Otwórz drugi projekt w osobnym oknie VS
2. Wybierz profil: InventoryService (Project)
3. Uruchom: Ctrl + F5
4. Test:
   http://localhost:5002/inventory/1
   http://localhost:5002/inventory/999


## Struktura projektu

ProductService/
  Program.cs
  Models/Product.cs
  Data/Seed.cs

InventoryService/
  Program.cs
  Models/InventoryItem.cs

## Cel projektu
Celem projektu jest pokazanie komunikacji między usługami w architekturze rozproszonej (.NET 8 Minimal API).
