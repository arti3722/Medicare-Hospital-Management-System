# Medicare HMS - Setup (MERN: Patient + Doctor + Admin panels)


## 1. Free accounts (keys)
- MongoDB Atlas (free cluster) -> MONGODB_URI
- Cloudinary (free) -> CLOUDINARY_NAME / API_KEY / SECRET_KEY
- Payment (Razorpay/Stripe) optional

## 2. Env files
Har folder mein `.env.example` ko copy karke `.env` banao aur values bharo:
backend/.env , frontend/.env , admin/.env

## 3. Run (3 alag terminal)
cd backend  && npm install && npm run server    (http://localhost:4000)
cd frontend && npm install && npm run dev       (Patient site)
cd admin    && npm install && npm run dev       (Admin + Doctor panel)

## 4. Login
Admin: backend/.env wale ADMIN_EMAIL / ADMIN_PASSWORD (admin panel mein)
Pehle admin se doctor add karo (photo ke liye Cloudinary zaroori), phir
doctor ko admin panel se login karwao; patient frontend par sign up karega.

## Flow (viva ke liye)
Admin doctor add -> Patient register/login -> doctor + slot chuna -> appointment book
-> Doctor panel se status (complete/cancel) -> Admin dashboard mein counts/earnings.
