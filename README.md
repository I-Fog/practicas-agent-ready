# practicas-agent-ready

Repositorio de referencia para practicas universitarias pequenas.

El objetivo es mantener ejemplos didacticos en varios lenguajes y documentar como un repositorio educativo puede prepararse para trabajo con agentes de codigo.

Este repositorio sirve como adopcion publica de [`codex-study-oss-kit`](https://github.com/I-Fog/codex-study-oss-kit): el cambio agent-ready se incorpora mediante pull request para que el flujo de mantenimiento sea visible.

## Practicas

- [`practicas/python-basics`](practicas/python-basics): listas, filtros y tests con `unittest`.
- [`practicas/cpp-basics`](practicas/cpp-basics): vectores, acumuladores y un test C++ minimo.

## Validacion

```bash
codex-study audit practicas/python-basics
codex-study audit practicas/cpp-basics
cd practicas/python-basics && python -m unittest discover -s tests && cd ../..
mkdir -p build && g++ -std=c++17 -I practicas/cpp-basics/src practicas/cpp-basics/tests/test_sumar_pares.cpp -o build/test_sumar_pares && ./build/test_sumar_pares
```

## Agent-readiness workflow

El workflow de GitHub Actions instala `codex-study-oss-kit`, audita las practicas y publica un resumen en las pull requests del propio repositorio.
