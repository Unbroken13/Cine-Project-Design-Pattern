# 🎬 Cinema Booking System

## 📝 Description
This project implements the core logical engine (in-memory backend) for a cinema reservation and billing system. It is designed with a strong focus on **Object-Oriented Programming (OOP)**, **SOLID principles**, and **Design Patterns** to ensure a scalable and maintainable architecture.

The main objective is to solve the domain complexity of reservations (preventing seat collisions across different showtimes) and manage a dynamic pricing system through clean architecture.

## ✨ Key Features
* **Spacetime Management:** Implementation of the `Proyeccion` (Showtime) entity to decouple physical seats (`Asientos`) from schedules, allowing multiple functions in the same room (`Sala`).
* **Dynamic Pricing Engine:** Utilization of the **Decorator** pattern to calculate the final price of the `Ticket`. It allows stacking dynamic surcharges (e.g., +20% for Premieres, +$1500 for Premium Rooms, +5% App Service Fee) while respecting the *Open/Closed Principle*.
* **Sales Manager (Controller):** Centralized and independent business logic (*Stateless* approach) via `GestorVenta`, separating data state from purchasing actions.

## 🏗️ Architecture & Domain Model
The system is composed of the following main entities:
* `Cine` -> `Sala` -> `Asiento` (Physical structure via Composition).
* `Proyeccion` (Binds a `Pelicula`, a `Sala`, and a Schedule, managing the reservation state).
* `Ticket` (Immutable receipt associating a `Cliente`, a `Proyeccion`, and an `Asiento`).
* `GestorVenta` (Domain service responsible for orchestration and validation).

## 🛠️ Tech Stack
* **Language:** Java (Core / Vanilla)
* **Libraries/Frameworks:** None (Zero-dependency architecture for educational focus)
* **Paradigm:** Object-Oriented Programming (OOP)

## 🚀 Installation and Execution
1. Clone the repository:
   ```bash
   git clone <repository-url>


---
ESPAÑOL

# 🎬 Sistema de Reservas de Cine (Cinema Booking System)

## 📝 Descripción
Este proyecto implementa el motor lógico central (backend en memoria) para la gestión de reservas y facturación de un cine. Está diseñado con un fuerte enfoque en **Programación Orientada a Objetos (POO)**, principios **SOLID** y **Patrones de Diseño** para garantizar una arquitectura escalable y mantenible.

El objetivo principal es resolver la complejidad del dominio de reservas (evitando la colisión de asientos en diferentes horarios) y gestionar un sistema dinámico de precios mediante arquitectura limpia.

## ✨ Características Principales
* **Manejo del Espacio-Tiempo:** Implementación de la entidad `Proyeccion` para desacoplar las butacas físicas (`Asientos`) de los horarios, permitiendo múltiples funciones en una misma `Sala`.
* **Motor de Precios Dinámico:** Utilización del patrón **Decorator** para calcular el precio final del `Ticket`. Permite apilar recargos dinámicos (Ej: +20% por Estreno, +$1500 por Sala Premium, +5% cargo por App) respetando el principio *Open/Closed*.
* **Gestor de Ventas (Controlador):** Lógica de negocio centralizada e independiente del estado (*Stateless*) a través de `GestorVenta`, separando los datos de las acciones de compra.

## 🏗️ Arquitectura y Modelo de Dominio
El sistema está compuesto por las siguientes entidades principales:
* `Cine` -> `Sala` -> `Asiento` (Estructura física mediante Composición).
* `Proyeccion` (Une una `Pelicula`, una `Sala` y un Horario, manteniendo el estado de las reservas).
* `Ticket` (Comprobante inmutable que asocia a un `Cliente`, una `Proyeccion` y un `Asiento`).
* `GestorVenta` (Servicio de dominio encargado de la orquestación y validación).

## 🛠️ Stack Tecnológico
* **Lenguaje:** Java (Core / Vanilla)
* **Librerías/Frameworks:** Ninguna (Arquitectura cero dependencias para enfoque educativo)
* **Paradigma:** Programación Orientada a Objetos (POO)

