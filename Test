import { useEffect } from "react";
import { BrowserRouter as Router, Routes, Route, Link } from "react-router-dom";
import { motion } from "framer-motion";

// Dummy components for now
const testimonials = [
  {
    quote:
      "I always knew I had the knowledge, but Elevatr gave me the confidence to say it in a way that stuck. I finally landed a job I’m proud of.",
    name: "Arya, B.Tech Final Year"
  },
  {
    quote:
      "I thought soft skills were just theory until I experienced Elevatr. The mock interviews, the STAR answers, and daily practice — it changed the game for me.",
    name: "Vishnu, MBA Student"
  }
];

function Home() {
  return (
    <div className="px-6 py-10 max-w-6xl mx-auto">
      <motion.h1
        initial={{ opacity: 0, y: -50 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
        className="text-4xl font-bold text-center text-purple-800"
      >
        Confidence is the New Qualification
      </motion.h1>

      <p className="mt-6 text-center text-lg max-w-2xl mx-auto">
        Elevatr is a 6-week career accelerator that blends real-world simulations,
        confidence-building exercises, and expert-backed strategies to transform placement outcomes.
      </p>

      <div className="mt-12 grid gap-8 md:grid-cols-2">
        {testimonials.map((t, i) => (
          <motion.div
            key={i}
            className="bg-white shadow-xl rounded-2xl p-6 border"
            initial={{ opacity: 0, y: 30 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ delay: i * 0.2 }}
          >
            <p className="text-lg italic">“{t.quote}”</p>
            <p className="mt-4 font-semibold text-right">— {t.name}</p>
          </motion.div>
        ))}
      </div>

      <div className="text-center mt-12">
        <Link to="/signup">
          <motion.button
            whileHover={{ scale: 1.05 }}
            whileTap={{ scale: 0.95 }}
            className="bg-purple-700 text-white px-6 py-3 rounded-full text-lg shadow-md hover:bg-purple-800"
          >
            Book a Free Discovery Call
          </motion.button>
        </Link>
      </div>
    </div>
  );
}

function SignUp() {
  return (
    <div className="p-10 text-center">
      <h2 className="text-2xl font-bold mb-6">Sign Up / Enquiry</h2>
      <form className="max-w-md mx-auto space-y-4">
        <input className="w-full p-3 border rounded" placeholder="Full Name" />
        <input className="w-full p-3 border rounded" placeholder="Email" />
        <input className="w-full p-3 border rounded" placeholder="Phone Number" />
        <button className="w-full bg-purple-700 text-white p-3 rounded hover:bg-purple-800">
          Submit
        </button>
      </form>
    </div>
  );
}

function AboutUs() {
  return (
    <div className="p-10 max-w-4xl mx-auto">
      <h2 className="text-2xl font-bold text-center">About Us</h2>
      <p className="mt-6 text-lg text-center">
        Elevatr is a bold new take on placement prep. Built by career coaches, HR leaders, and hiring managers,
        we’re on a mission to make confidence the core skillset for modern careers.
      </p>
    </div>
  );
}

function App() {
  return (
    <Router>
      <nav className="bg-white shadow p-4 flex justify-between items-center px-6">
        <Link to="/" className="font-bold text-purple-700 text-xl">
          Elevatr
        </Link>
        <div className="space-x-4">
          <Link to="/">Home</Link>
          <Link to="/signup">Sign Up</Link>
          <Link to="/about">About Us</Link>
        </div>
      </nav>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/signup" element={<SignUp />} />
        <Route path="/about" element={<AboutUs />} />
      </Routes>
    </Router>
  );
}

export default App;
