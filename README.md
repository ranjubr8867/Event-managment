# Event-managment

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Eventify | Event Management</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', sans-serif;
    scroll-behavior: smooth;
}

body {
    background: #0d0d18;
    color: white;
}

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 22px 8%;
    background: #151526;
    position: sticky;
    top: 0;
    z-index: 100;
}

.logo {
    font-size: 27px;
    font-weight: bold;
    color: #ff6b9d;
}

nav a {
    color: white;
    text-decoration: none;
    margin-left: 25px;
    font-size: 14px;
}

nav a:hover {
    color: #ff6b9d;
}

.hero {
    min-height: 85vh;
    display: flex;
    align-items: center;
    padding: 8%;
    background:
    linear-gradient(90deg, rgba(13,13,24,.95), rgba(13,13,24,.45)),
    url('https://images.unsplash.com/photo-1492684223066-81342ee5ff30?w=1600')
    center/cover;
}

.hero-content {
    max-width: 650px;
}

.hero h1 {
    font-size: clamp(42px, 6vw, 70px);
    line-height: 1.1;
    margin-bottom: 20px;
}

.hero h1 span {
    color: #ff6b9d;
}

.hero p {
    color: #ddd;
    line-height: 1.8;
    margin-bottom: 30px;
}

.btn {
    display: inline-block;
    padding: 13px 25px;
    background: #ff6b9d;
    color: white;
    border: none;
    border-radius: 7px;
    text-decoration: none;
    cursor: pointer;
    font-weight: bold;
}

.btn:hover {
    background: #e64b83;
}

section {
    padding: 75px 8%;
}

.section-title {
    text-align: center;
    font-size: 35px;
    margin-bottom: 15px;
}

.subtitle {
    text-align: center;
    color: #aaa;
    margin-bottom: 40px;
}

.categories, .events {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(220px,1fr));
    gap: 25px;
}

.category, .event-card {
    background: #1b1b30;
    border-radius: 12px;
    overflow: hidden;
    transition: .3s;
}

.category {
    padding: 30px;
    text-align: center;
}

.category:hover, .event-card:hover {
    transform: translateY(-7px);
    background: #262641;
}

.category .emoji {
    font-size: 42px;
    margin-bottom: 15px;
}

.event-card img {
    width: 100%;
    height: 190px;
    object-fit: cover;
}

.event-info {
    padding: 20px;
}

.event-info h3 {
    margin-bottom: 10px;
}

.event-info p {
    color: #aaa;
    margin-bottom: 15px;
    font-size: 14px;
}

.booking {
    background: #151526;
}

.booking-form {
    max-width: 600px;
    margin: auto;
    background: #202039;
    padding: 30px;
    border-radius: 12px;
}

.booking-form input,
.booking-form select,
.booking-form textarea {
    width: 100%;
    padding: 13px;
    margin: 10px 0 18px;
    border: 1px solid #444;
    background: #111120;
    color: white;
    border-radius: 6px;
}

.booking-form label {
    color: #ddd;
}

.booking-form button {
    width: 100%;
}

.about {
    text-align: center;
    max-width: 850px;
    margin: auto;
    color: #ccc;
    line-height: 1.9;
}

footer {
    text-align: center;
    padding: 30px;
    background: #090912;
    color: #aaa;
}

#message {
    text-align: center;
    margin-top: 15px;
    color: #79e6a0;
}
</style>
</head>

<body>

<header>
    <div class="logo">Eventify ✦</div>
    <nav>
        <a href="#home">Home</a>
        <a href="#categories">Categories</a>
        <a href="#events">Events</a>
        <a href="#booking">Book Now</a>
        <a href="#about">About</a>
    </nav>
</header>

<section class="hero" id="home">
    <div class="hero-content">
        <h1>Make Every Moment <span>Memorable.</span></h1>
        <p>
            From unforgettable celebrations to professional gatherings,
            Eventify makes planning your perfect event simple,
            creative and stress-free.
        </p>
        <a href="#events" class="btn">Explore Events</a>
        <a href="#booking" class="btn">Book an Event</a>
    </div>
</section>

<section id="categories">
    <h2 class="section-title">Event Categories</h2>
    <p class="subtitle">Every occasion deserves something special.</p>

    <div class="categories">
        <div class="category">
            <div class="emoji">💍</div>
            <h3>Weddings</h3>
            <p>Beautiful wedding celebrations.</p>
        </div>

        <div class="category">
            <div class="emoji">🎂</div>
            <h3>Birthdays</h3>
            <p>Celebrate your special day.</p>
        </div>

        <div class="category">
            <div class="emoji">🎓</div>
            <h3>College Events</h3>
            <p>Festivals, fests and parties.</p>
        </div>

        <div class="category">
            <div class="emoji">🏢</div>
            <h3>Corporate</h3>
            <p>Professional events and meetings.</p>
        </div>
    </div>
</section>

<section id="events">
    <h2 class="section-title">Popular Events</h2>
    <p class="subtitle">Discover experiences worth remembering.</p>

    <div class="events">

        <div class="event-card">
            <img src="https://images.unsplash.com/photo-1511795409834-ef04bbd61622?w=700">
            <div class="event-info">
                <h3>Grand Wedding</h3>
                <p>📍 Luxury Celebration Hall</p>
                <p>✨ Elegant decorations and celebrations.</p>
                <button class="btn" onclick="selectEvent('Grand Wedding')">Book Now</button>
            </div>
        </div>

        <div class="event-card">
            <img src="https://images.unsplash.com/photo-1530103862676-de8c9debad1d?w=700">
            <div class="event-info">
                <h3>Birthday Bash</h3>
                <p>📍 Celebration Arena</p>
                <p>🎉 Make birthdays unforgettable.</p>
                <button class="btn" onclick="selectEvent('Birthday Bash')">Book Now</button>
            </div>
        </div>

        <div class="event-card">
            <img src="https://images.unsplash.com/photo-1506157786151-b8491531f063?w=700">
            <div class="event-info">
                <h3>Music Festival</h3>
                <p>📍 Open Air Arena</p>
                <p>🎵 Music, lights and entertainment.</p>
                <button class="btn" onclick="selectEvent('Music Festival')">Book Now</button>
            </div>
        </div>

    </div>
</section>

<section class="booking" id="booking">
    <h2 class="section-title">Book Your Event</h2>
    <p class="subtitle">Tell us about your dream event.</p>

    <form class="booking-form" id="bookingForm">
        <label>Full Name</label>
        <input type="text" id="name" placeholder="Enter your name" required>

        <label>Email Address</label>
        <input type="email" id="email" placeholder="Enter your email" required>

        <label>Phone Number</label>
        <input type="tel" id="phone" placeholder="Enter phone number"
        pattern="[0-9]{10}" required>

        <label>Event Type</label>
        <select id="eventType" required>
            <option value="">Select an event</option>
            <option>Wedding</option>
            <option>Birthday</option>
            <option>College Event</option>
            <option>Corporate Event</option>
            <option>Music Festival</option>
            <option>Grand Wedding</option>
            <option>Birthday Bash</option>
        </select>

        <label>Event Date</label>
        <input type="date" id="date" required>

        <label>Number of Guests</label>
        <input type="number" id="guests" min="1" placeholder="Number of guests" required>

        <label>Additional Details</label>
        <textarea id="details" rows="4" placeholder="Describe your event..."></textarea>

        <button type="submit" class="btn">Submit Booking</button>
        <p id="message"></p>
    </form>
</section>

<section id="about">
    <h2 class="section-title">About Eventify</h2>
    <p class="about">
        Eventify is an event management platform designed to make
        event planning easier and more organized. Whether it is a
        wedding, birthday, college fest or corporate gathering,
        our platform helps users explore event options and submit
        booking requests in one convenient place.
        Our goal is to turn every idea into a memorable experience.
    </p>
</section>

<footer>
    <p>© 2026 Eventify. All Rights Reserved.</p>
    <p>Creating Moments. Making Memories. ✨</p>
</footer>

<script>
function selectEvent(event) {
    document.getElementById("eventType").value =
        event === "Grand Wedding" ? "Wedding" :
        event === "Birthday Bash" ? "Birthday" : event;

    document.getElementById("booking").scrollIntoView({
        behavior: "smooth"
    });
}

document.getElementById("date").min =
    new Date().toISOString().split("T")[0];

document.getElementById("bookingForm").addEventListener("submit",
function(e) {
    e.preventDefault();

    const booking = {
        id: "EVT" + Date.now(),
        name: document.getElementById("name").value,
        email: document.getElementById("email").value,
        phone: document.getElementById("phone").value,
        event: document.getElementById("eventType").value,
        date: document.getElementById("date").value,
        guests: document.getElementById("guests").value,
        details: document.getElementById("details").value
    };

    let bookings = JSON.parse(localStorage.getItem("eventBookings")) || [];
    bookings.push(booking);
    localStorage.setItem("eventBookings", JSON.stringify(bookings));

    document.getElementById("message").innerText =
        "Booking request submitted successfully! Your ID: " + booking.id;

    this.reset();
});
</script>

</body>
</html>
