flex-store/
├── frontend/
│   ├── pages/
│   ├── components/
│   └── styles/
├── backend/
│   ├── models/
│   ├── routes/
│   ├── controllers/
│   └── server.js
└── README.md
```
// pages/index.js
export default function Home() {
  return (
    <div className="min-h-screen bg-slate-900 text-white">
      <header className="p-6 text-center">
        <h1 className="text-4xl font-bold">Flex Store</h1>
        <p className="mt-2 text-blue-400">متجر فلكس للمنتجات الرقمية</p>
      </header>

      <main className="grid grid-cols-1 md:grid-cols-3 gap-6 p-6">
        <div className="bg-slate-800 p-4 rounded">كتاب إلكتروني</div>
        <div className="bg-slate-800 p-4 rounded">كورس تدريبي</div>
        <div className="bg-slate-800 p-4 rounded">قالب تصميم</div>
      </main>
    </div>
  );
}
```

// backend/server.js
const express = require('express');
const mongoose = require('mongoose');
const app = express();

app.use(express.json());

mongoose.connect('mongodb://localhost/flexstore');

app.get('/', (req, res) => {
  res.send('Flex Store API Running');
});

app.listen(5000, () => console.log('Server running on port 5000'));
``

