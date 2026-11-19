# 0008 · Supabase: Postgres, Auth y RLS

- **Estado:** Aceptada
- **Fecha:** 2026-11-19
- **Versión:** (se anota al instalar)

## Contexto
Habrá datos de salud sensibles. En CineExplorer el JWT tenía un secreto de respaldo en el código y el token vivía en localStorage.

## Decisión
Supabase para la base de datos (Postgres), la autenticación por correo y Row Level Security (RLS) en cada tabla. La API verifica el JWT de Supabase.

## Por qué
Ahorra semanas. RLS es un segundo candado además de la API. El SDK renueva el token y avisa cuando cambia la sesión.

## Alternativas consideradas
- **Autenticación propia con JWT:** más trabajo y más riesgo.
- **Firebase:** no es SQL; el RLS de Postgres encaja mejor con datos relacionales.

## Consecuencias
En el plan gratuito los proyectos pueden pausarse por inactividad y los límites cambian: revisarlos antes de lanzar.
