# CropSync - SIH 2026 frontend prototype

CropSync is a role-based direct marketplace that addresses SIH26033: reducing intermediary layers between farmers and consumers. This frontend prototype demonstrates the key experience from the attached proposal:

- Consumer: discover direct-from-farm produce, search, add items to a basket, place a prototype order, and view their impact.
- Farmer: view sales, active orders, fair-price score, and AI-backed market recommendations.
- Admin / Logistics: see delivery-route health, active farmers, quality verification, and order operations.
- Traceability: a farm-to-kitchen batch card showing farm, harvest time, and planned delivery.

## Run locally in VS Code

1. Install [Node.js LTS](https://nodejs.org/) (version 20 or newer).
2. In VS Code, use **File > Open Folder** and choose this `build-x20-2` folder.
3. Open **Terminal > New Terminal** and run:

   ```powershell
   npm install
   npm run dev
   ```

4. Open the localhost URL shown in the terminal (normally `http://localhost:5173`).
5. Press `Ctrl+C` in the terminal to stop the server.

To create a production build, run:

```powershell
npm run build
```

## Git commands

Run these from the VS Code terminal to create your first repository commit:

```powershell
git init
git add .
git commit -m "Build CropSync SIH frontend prototype"
```

Then create an empty GitHub repository and connect it:

```powershell
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/cropsync.git
git push -u origin main
```

## Notes for the next stage

The current app uses frontend demo data deliberately, so it can be presented without a backend. The intended integration points map directly to the technical approach in the proposal: FastAPI/JWT for role enforcement, PostgreSQL for users/products/orders, price and demand services, QR batch data, and logistics APIs. Keep authorization enforcement on the backend as well - the role picker here is only a prototype view switcher.
