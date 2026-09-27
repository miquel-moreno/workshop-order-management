# Workshop Order Management

Panel en producción para los pedidos de un taller de chapa: entran por oficina, correo o móvil y se siguen de *Pendiente* a *Entregado*.

> Demo disponible bajo petición.

![Panel del taller](./docs/images/prod-panel-taller.png)

## Qué hace

- Reúne los pedidos de **tres canales** en un solo panel, actualizado en tiempo real.
- Genera la **ficha y la etiqueta en PDF** automáticamente ([flujo de n8n](https://github.com/miquel-moreno/n8n-order-automation)).
- **Roles** separados para montadores, administración y almacén.

## Este repositorio

Contiene el **motor de entrada de pedidos**: convierte un mensaje en texto libre en un pedido con su prioridad.

> «Pedido 90234, lo necesito hoy. 400x200 e=2mm, 2 pliegues r=3mm. RAL 9016.»
> → nº de pedido, fecha de entrega, prioridad crítica, medidas, pliegues y color.

```bash
cd backend
npm install
npm run seed   # datos ficticios
npm start      # http://localhost:4000
npm test
```

## Stack

**Producción:** JavaScript · PostgreSQL con tiempo real · n8n + Gotenberg
**Este repositorio:** Node.js · Express · SQLite

## Mi papel

Diseño y desarrollo de la mayor parte del proyecto: flujo de pedidos, panel, documentos y puesta en producción. Desarrollo asistido por IA bajo mi especificación y revisión.

---

[Perfil](https://github.com/miquel-moreno) · [LinkedIn](https://www.linkedin.com/in/miquel-moreno-martinez)