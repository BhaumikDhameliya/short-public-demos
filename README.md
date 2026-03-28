## Future Workflow (Every New Demo)

When you win a new bid and build a new demo, the entire workflow is:

```bash
# 1. Create folder for the new demo
mkdir crypto-payment-demo

# 2. Drop your HTML file in as index.html
mv new_demo.html crypto-payment-demo/index.html

# 3. Add a link in root index.html (optional but good practice)

# 4. Push
git add .
git commit -m "Add: crypto payment checkout demo"
git push origin main

# 5. URL is live in ~60 seconds:
# https://YOUR_USERNAME.github.io/freelance-demos/crypto-payment-demo/
```