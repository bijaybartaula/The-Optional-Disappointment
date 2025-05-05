# **I Tried to Build a Web App in a Weekend. I Ended Up With Technical Debt and Regret.**

### A weekend sprint that started with optimism and ended with valuable lessons.

---

## **Monday Morning: Reflection and Realization**

It’s Monday morning, and I’m sitting in front of my computer, my mind swirling with the remnants of a weekend spent coding. What was supposed to be a simple web app to track household groceries has turned into a tangled mess of unfinished features, buggy code, and unmet expectations.

I had grand plans. In my head, I was going to build something useful, polished, and even shareable. The idea seemed simple enough—a web app to track groceries and supplies at home. No more buying duplicates, no more forgotten pantry items. A simple solution to an everyday problem.

But what I ended up with was an exercise in overestimating my abilities, underestimating complexity, and, ultimately, learning how quickly technical debt can accumulate when rushing toward a deadline.

---

## **Friday Evening: The Genesis of an Idea**

### 5:00 PM – The Inspiration

The idea for my app came from a very real, everyday frustration: how easy it is to forget what groceries I already have in stock. This is a problem that resonates with many, especially in Nepal, where supply chains can be unpredictable, prices fluctuate, and shortages are common. I’ve found myself buying the same items repeatedly, simply because I wasn’t able to keep track of what was already in my pantry.

With this in mind, I thought, *Why isn’t there a simple web app to help households in Nepal track groceries and supplies?* An app that can help people manage inventory, save money, reduce food waste, and streamline shopping habits. It felt like the perfect weekend project.

I imagined a simple yet functional app:

* **Frontend:** React for its speed and flexibility.
* **Backend:** Supabase, for a simple yet powerful PostgreSQL-based database.
* **Authentication:** Clerk for easy user management and authentication.
* **UI:** ShadCN for a modern and customizable UI component library that would make the design process faster and smoother.

I set out to have the app built, tested, and deployed by Sunday night. How hard could it be?

---

## **Saturday: The Build Begins**

### 9:00 AM – Getting Started

I opened VSCode and ran the following command to set up the project using TypeScript:

```bash
npx create-react-app my-app --template typescript
```

This command created a React app with TypeScript out of the box, which was a crucial step. TypeScript helps with type safety and enhances code maintainability, which would come in handy as the project grew in complexity. Once the setup was complete, I quickly set up the basic folder structure. React was responsive and familiar, and I was feeling confident. I integrated Supabase early on to handle the database, and the authentication part was made straightforward with Clerk.

Here’s a rundown of the tools and technologies I chose:

* **Frontend Library:** React
  React was the natural choice for the frontend, given its flexibility and the ease with which it allows me to build dynamic UIs. React’s component-based architecture helped structure the app well, but I failed to focus on clean, modular code early on.

* **Backend & Database:** Supabase
  Supabase offers an open-source alternative to Firebase and seemed like the perfect fit. It’s essentially a backend-as-a-service that provides a real-time PostgreSQL database, authentication, and storage solutions out of the box. This saved me from having to manually configure everything.

* **Authentication:** Clerk
  Authentication can often be a pain to implement correctly, but Clerk made it simple. With its easy integration and focus on secure, user-centric authentication, it was the right choice for my app.

* **UI Library:** ShadCN
  I decided to use ShadCN for UI components. The library is highly customizable, modern, and fast, which aligned well with the project’s need for quick iteration without sacrificing design quality.

### 1:00 PM – The First Hurdles

Everything was going according to plan until I hit a wall with Supabase authentication. Clerk had made the process easy, but I had forgotten a small but crucial step: setting up the email verification properly. This created a lot of confusion early on, especially when the user flow didn’t work as expected. I spent a few hours trying to debug the issue, eventually realizing it was a simple configuration mistake.

Once that was fixed, I was back on track. I continued by building out the app’s core functionality: adding and removing items from the inventory, setting expiration dates, and categorizing items by type. The database schema was simple, but I quickly realized how critical it was to structure the data well upfront. I spent the next few hours fine-tuning the schema to make sure it could scale.

### 5:00 PM – UI Design and ShadCN

Next up was the UI. I had heard good things about ShadCN, and after a quick review of its components and documentation, I decided to give it a try. The library was lightweight, customizable, and easy to integrate into the project. It was also beautifully designed, which meant I didn’t have to spend too much time on styling.

But here’s where I made my first mistake. I tried to get too fancy, thinking I could quickly build out multiple pages with advanced animations and transitions. While ShadCN gave me the tools, I lost a lot of time on details that weren’t essential to the core functionality. Buttons weren’t aligning properly, modals were closing too slowly, and responsiveness wasn’t perfect.

I spent hours on these smaller UI issues, all the while losing sight of the fact that the app was supposed to be functional first, not polished.

---

## **Sunday: The Final Push (and the Realization)**

### 9:30 AM – Feature Creep

By Sunday morning, I realized my time was running out. I had added a few extra features I wasn’t sure were necessary: barcode scanning for inventory updates, a reminder system for expiring items, and a visual dashboard for pantry stats. None of these were critical to the app’s core functionality, but I wanted to add them because they seemed like the kind of “wow factor” that would make the app stand out.

I spent several hours trying to integrate a barcode scanning library. It was supposed to be easy, but it turned out to be far more complex than I anticipated. It didn’t support all devices properly, permissions were a mess, and the error handling was abysmal. I wasted a lot of time debugging issues that were secondary to the main goal of simply tracking items in the pantry.

### 3:00 PM – The Realization

At some point, I realized that I had strayed too far from the initial goal of building a simple app. I had tried to do too much in too little time. Instead of focusing on making the core features solid, I got distracted by things like barcode scanning and unnecessary UI tweaks.

I had forgotten a crucial principle: **start small and iterate.** Instead of adding bells and whistles, I should have focused on refining the core functionality—making sure the add/remove feature worked flawlessly, that the database synced properly, and that the UI was intuitive.

### 9:00 PM – Deployment

I pushed the app live to Supabase and Firebase Hosting. The deployment went smoothly, and I was able to get everything online. However, when I tried using the app on my phone, I encountered several bugs I hadn’t noticed during testing. The layout was off on mobile, state management was lagging in some places, and the reminder system only worked intermittently.

At that moment, I realized that while I had a working product, it wasn’t the polished, finished app I had imagined. It was a prototype—something that could be useful, but needed a lot more work.

---

## **Tools, Libraries, and Frameworks Used**

### **Frontend:**

* **React with TypeScript:**
  To initialize the project with TypeScript, I used `npx create-react-app my-app --template typescript`, which helped ensure type safety and better code quality from the start. React’s flexibility allowed for rapid development of dynamic UIs.

* **ShadCN UI Library:**
  A lightweight, modern UI library that helped me speed up development. ShadCN provided customizable, ready-to-use components that fit well with the app’s design goals.

### **Backend and Database:**

* **Supabase:**
  I used Supabase as the backend service to handle database queries, real-time updates, and authentication. It’s built on top of PostgreSQL, which made it easy to manage the app’s inventory data while also providing real-time sync.

* **Supabase Authentication:**
  For handling user authentication securely and seamlessly, Supabase’s built-in authentication system made login, signup, and user management a breeze.

### **Authentication:**

* **Clerk:**
  Clerk provided an easy way to manage user authentication. It saved me time by handling user sessions, social logins, and email verification out-of-the-box.

### **API Integrations:**

* **Supabase REST API:**
  The app’s backend calls were handled by Supabase’s RESTful API, which allowed for seamless data retrieval, updates, and real-time sync across devices.

### **Testing and Debugging:**

* **React Developer Tools & Supabase Dashboard:**
  I used these tools to debug UI issues and monitor database queries in real-time. However, I failed to implement automated testing, which would have helped catch issues earlier in the process.

---

## **Lessons Learned**

### 1. **Scope Your Project Carefully**

The biggest lesson I learned from this project is to be realistic about what can be accomplished in a short amount of time. I tried to do too much. If I had focused on just one or two key features and refined them, I would have ended up with a much more polished product.

### 2. **Use What You Know**

While Supabase and Clerk were great choices, I should have stuck to libraries and tools I was already familiar with, especially under a tight deadline. Trying to learn new tools while building the app was a recipe for disaster.

### 3. **UI is Important, but Don’t Lose Sight of Functionality**

ShadCN helped me create a beautiful UI, but I got too caught up in making everything look perfect. The core functionality should always come first. In the future, I’ll focus more on ensuring the app works perfectly before worrying about fine-tuning the design.

### 4. **Test Early and Often**

Testing early would have saved me hours of frustration. I didn’t test the app properly across devices until the end, and by then, many bugs had accumulated. More testing would have caught these issues earlier.

---

## **Would I Do It Again?**

In short: yes.

But I would approach it differently. I’d start smaller, keep the scope manageable, and focus on a simpler, more effective solution before diving into complexity. I’d also spend more time planning, designing, and testing before diving into development.

Building something useful is always a rewarding experience, even if the result isn’t exactly what you imagined. I learned a lot in a short amount of time, and that’s what matters the most.

