import { BrowserRouter as Router, Routes, Route } from "react-router-dom";
import Home from "./pages/Home";
import Products from "./pages/Products";
import About from "./pages/About";
import Contact from "./pages/Contact";
import Login from "./pages/Login";
import Register from "./pages/Register";
import AdminPanel from "./pages/AdminPanel";
import Navbar from "./components/Navbar";
import Footer from "./components/Footer";

export default function App() {
  return (
    <Router>
      <div className="min-h-screen flex flex-col bg-gray-100 text-gray-900">
        <Navbar />
        <main className="flex-grow">
          <Routes>
            <Route path="/" element={<Home />} />
            <Route path="/products" element={<Products />} />
            <Route path="/about" element={<About />} />
            <Route path="/contact" element={<Contact />} />
            <Route path="/login" element={<Login />} />
            <Route path="/register" element={<Register />} />
            <Route path="/admin" element={<AdminPanel />} />
          </Routes>
        </main>
        <Footer />
      </div>
    </Router>
  );
}

// components/Navbar.jsx
export function Navbar() {
  return (
    <nav className="bg-white shadow-md p-4 flex justify-between items-center">
      <h1 className="text-2xl font-bold text-blue-600">Æ Sport™</h1>
      <div className="space-x-4">
        <a href="/" className="hover:text-blue-500">Inicio</a>
        <a href="/products" className="hover:text-blue-500">Productos</a>
        <a href="/about" className="hover:text-blue-500">Sobre Nosotros</a>
        <a href="/contact" className="hover:text-blue-500">Contacto</a>
        <a href="/login" className="hover:text-blue-500">Login</a>
      </div>
    </nav>
  );
}

// components/Footer.jsx
export function Footer() {
  return (
    <footer className="bg-gray-800 text-white p-4 text-center">
      <p>&copy; 2025 Æ Sport™. Todos los derechos reservados.</p>
    </footer>
  );
}

// pages/Home.jsx
export default function Home() {
  return (
    <section className="p-6 text-center">
      <h2 className="text-3xl font-bold mb-4">Bienvenido a Æ Sport™</h2>
      <p className="text-lg">Tu tienda en línea de ropa, tecnología, herramientas y servicios técnicos.</p>
    </section>
  );
}

// pages/Products.jsx
export default function Products() {
  return (
    <section className="p-6">
      <h2 className="text-2xl font-bold mb-4">Nuestros Productos</h2>
      <p>Catálogo próximamente...</p>
    </section>
  );
}

// pages/About.jsx
export default function About() {
  return (
    <section className="p-6">
      <h2 className="text-2xl font-bold mb-4">Sobre Nosotros</h2>
      <p>Æ Sport™ nace con la visión de combinar estilo, tecnología y soporte técnico en un solo lugar.</p>
    </section>
  );
}

// pages/Contact.jsx
export default function Contact() {
  return (
    <section className="p-6">
      <h2 className="text-2xl font-bold mb-4">Contáctanos</h2>
      <form className="space-y-4 max-w-md mx-auto">
        <input type="text" placeholder="Nombre" className="w-full p-2 border rounded" />
        <input type="email" placeholder="Correo" className="w-full p-2 border rounded" />
        <textarea placeholder="Mensaje" className="w-full p-2 border rounded"></textarea>
        <button type="submit" className="bg-blue-600 text-white px-4 py-2 rounded">Enviar</button>
      </form>
    </section>
  );
}

// pages/Login.jsx
export default function Login() {
  return (
    <section className="p-6 max-w-md mx-auto">
      <h2 className="text-2xl font-bold mb-4">Iniciar Sesión</h2>
      <form className="space-y-4">
        <input type="email" placeholder="Correo" className="w-full p-2 border rounded" />
        <input type="password" placeholder="Contraseña" className="w-full p-2 border rounded" />
        <button type="submit" className="bg-blue-600 text-white px-4 py-2 rounded">Entrar</button>
      </form>
    </section>
  );
}

// pages/Register.jsx
export default function Register() {
  return (
    <section className="p-6 max-w-md mx-auto">
      <h2 className="text-2xl font-bold mb-4">Registrarse</h2>
      <form className="space-y-4">
        <input type="text" placeholder="Nombre completo" className="w-full p-2 border rounded" />
        <input type="email" placeholder="Correo" className="w-full p-2 border rounded" />
        <input type="password" placeholder="Contraseña" className="w-full p-2 border rounded" />
        <button type="submit" className="bg-blue-600 text-white px-4 py-2 rounded">Crear cuenta</button>
      </form>
    </section>
  );
}

// pages/AdminPanel.jsx
export default function AdminPanel() {
  return (
    <section className="p-6">
      <h2 className="text-2xl font-bold mb-4">Panel de Administración</h2>
      <p>Aquí podrás gestionar tus productos. Funcionalidades próximamente...</p>
    </section>
  );
}
