# **Deploy a Static Website with a Contact Form Using Cloudflare Pages & FabForm**  



## **Step 1: Create Your Website**  

1. **Make a project folder:**  
   ```sh
   mkdir my-website && cd my-website
   ```  

2. **Create an `index.html` file:**  
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Contact Us</title>
       <script src="https://cdn.tailwindcss.com"></script>
   </head>
   <body class="flex items-center justify-center min-h-screen bg-gray-100">
       <form action="https://fabform.io/f/YOUR_FORM_ID" method="POST" class="bg-white p-6 rounded-lg shadow-lg w-96">
           <h1 class="text-2xl font-bold mb-4">Contact Us</h1>
           <input type="text" name="name" placeholder="Your Name" required class="w-full px-3 py-2 border rounded">
           <input type="email" name="email" placeholder="Your Email" required class="w-full px-3 py-2 border rounded">
           <textarea name="message" placeholder="Your Message" required class="w-full px-3 py-2 border rounded"></textarea>
           <button type="submit" class="w-full bg-blue-600 text-white py-2 rounded hover:bg-blue-700">Send</button>
       </form>
   </body>
   </html>
   ```  

3. Replace `YOUR_FORM_ID` with your **FabForm.io** form ID.  

---

## **Step 2: Set Up FabForm (Your Form Backend)**  

1. **Go to [FabForm.io](https://fabform.io/)**  
2. **Sign up & create a new form**  
3. **Copy the form URL** (e.g., `https://fabform.io/f/abcd1234`)  
4. **Paste it into your form's `action` in `index.html`**  

---

## **Step 3: Deploy to Cloudflare Pages**  

1. **Push your code to GitHub:**  
   ```sh
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/my-website.git
   git push -u origin main
   ```  

2. **Deploy on Cloudflare Pages:**  
   - Go to **[Cloudflare Pages](https://pages.cloudflare.com/)**  
   - Click **Create a Project**  
   - Connect your GitHub repo  
   - Select `main` branch & click **Deploy**  

---

## **Step 4: Test Your Form**  

- Visit your live website  
- Submit a test form  
- Check submissions on **[FabForm.io](https://fabform.io/)**  

---
