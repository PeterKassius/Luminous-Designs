# Luminous-Designs
we sell the newest and trendy street wear
from the lowest price u could ever imagine


const App = () => {
  return (
    <div className="bg-black text-white min-h-screen">
      {/* Header */}
      <header className="p-4 flex justify-between items-center border-b border-gray-700">
        <h1 className="text-2xl font-bold">StreetWear Co.</h1>
        <nav>
          <ul className="flex space-x-6">
            <li><a href="#collections" className="hover:text-gray-400">Collections</a></li>
            <li><a href="#about" className="hover:text-gray-400">About</a></li>
            <li><a href="#contact" className="hover:text-gray-400">Contact</a></li>
          </ul>
        </nav>
      </header>

      {/* Hero Section */}
      <section className="h-[70vh] flex items-center justify-center bg-[url('/hero-image.jpg')] bg-cover bg-center text-center">
        <div className="bg-black bg-opacity-60 p-6 rounded-lg">
          <h2 className="text-4xl font-bold">Elevate Your Street Style</h2>
          <p className="mt-2 text-gray-400">Shop the latest trends in urban fashion.</p>
          <Button className="mt-4 bg-white text-black px-6 py-2 font-semibold">Shop Now</Button>
        </div>
      </section>

      {/* Collections */}
      <section id="collections" className="p-8">
        <h3 className="text-3xl font-bold text-center mb-8">Featured Collections</h3>
        <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
          {["Hoodies", "T-Shirts", "Sneakers", "Jackets", "Accessories", "Caps"].map((item, index) => (
            <Card key={index} className="bg-gray-800 text-center">
              <img
                src={`/images/${item.toLowerCase()}.jpg`}
                alt={item}
                className="w-full h-40 object-cover rounded-t-lg"
              />
              <CardContent className="p-4">
                <h4 className="text-xl font-semibold">{item}</h4>
                <Button className="mt-4 bg-white text-black w-full">Explore</Button>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* About Section */}
      <section id="about" className="p-8 bg-gray-900">
        <div className="max-w-4xl mx-auto text-center">
          <h3 className="text-3xl font-bold">About Us</h3>
          <p className="mt-4 text-gray-400">
            StreetWear Co. is redefining urban fashion. We bring bold, trendsetting apparel 
            inspired by street culture and creativity. Join the movement and express your style.
          </p>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="p-8">
        <div className="max-w-lg mx-auto text-center">
          <h3 className="text-3xl font-bold">Get in Touch</h3>
          <form className="mt-6 space-y-4">
            <input
              type="text"
              placeholder="Your Name"
              className="w-full p-3 bg-gray-800 border border-gray-700 rounded"
            />
            <input
              type="email"
              placeholder="Your Email"
              className="w-full p-3 bg-gray-800 border border-gray-700 rounded"
            />
            <textarea
              placeholder="Your Message"
              rows="4"
              className="w-full p-3 bg-gray-800 border border-gray-700 rounded"
            ></textarea>
            <Button className="bg-white text-black w-full">Send Message</Button>
          </form>
        </div>
      </section>

      {/* Footer */}
      <footer className="p-4 text-center border-t border-gray-700">
        <p className="text-gray-500">&copy; {new Date().getFullYear()} StreetWear Co. All rights reserved.</p>
      </footer>
    </div>
  );
};

export default App;
