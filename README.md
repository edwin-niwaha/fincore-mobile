# 📱 FinCore Mobile

FinCore Mobile is a **client self-service mobile application** built with **React Native + TypeScript (Expo)**.

It connects directly to `fincore-api` and allows customers to securely manage their financial activities.

---

## 🚀 Purpose

FinCore Mobile enables clients to:

- View savings balances
- Track loans and repayments
- Apply for loans
- View transaction history
- Manage profile details
- Receive notifications
- Contact support

This app is strictly **client-facing** (not for staff/admin use).

---

## 🧱 Tech Stack

- React Native
- TypeScript
- Expo (recommended)
- React Navigation
- Axios (typed API client recommended)
- Expo SecureStore (secure token storage)
- Context API or Zustand (state management)

---

## 📁 Project Structure

```txt
fincore-mobile/
├── src/
│   ├── screens/
│   │   ├── auth/
│   │   ├── dashboard/
│   │   ├── savings/
│   │   ├── loans/
│   │   ├── transactions/
│   │   ├── profile/
│   │   └── support/
│   │
│   ├── components/
│   ├── navigation/
│   ├── lib/
│   │   ├── api/        # Typed API client
│   │   └── auth/       # Auth logic
│   ├── hooks/
│   ├── utils/
│   ├── types/
│   └── context/
│
├── App.tsx
├── app.json
├── .env.example

```

---

##  ⚙️ Setup
git clone https://github.com/your-org/fincore-mobile.git
cd fincore-mobile

npm install

cp .env.example .env

npx expo start

## 🌐 Environment Variables
EXPO_PUBLIC_API_BASE_URL=http://localhost:8000/api
EXPO_PUBLIC_API_BASE_URL=https://api.yourdomain.com/api

## 🔌 Connected API Endpoints
| Feature              | Method | Endpoint               |
| -------------------- | -----: | ---------------------- |
| Login                |   POST | `/auth/login/`         |
| Refresh token        |   POST | `/auth/refresh/`       |
| Logout               |   POST | `/auth/logout/`        |
| Profile              |    GET | `/auth/profile/`       |
| Client dashboard     |    GET | `/dashboards/client/`  |
| Savings accounts     |    GET | `/savings/accounts/`   |
| Savings transactions |    GET | `/transactions/`       |
| Loan applications    |    GET | `/loans/applications/` |
| Loan repayments      |    GET | `/loans/repayments/`   |
| Apply for loan       |   POST | `/loans/applications/` |
| Support messages     |   POST | `/support/`            |

