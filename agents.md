<!DOCTYPE html>
<html lang="en">

<body class="bg-gray-100 flex justify-center">
  <div class="container max-w-7xl">
    <header class="bg-white shadow p-4 flex justify-between items-center">
      <h1 class="text-2xl text-blue-600 font-bold">Synapster AI Marketplace</h1>
      <nav>
        <a href="/" class="mx-2 hover:text-blue-600">Home</a>
        <a href="/agents" class="mx-2 hover:text-blue-600">Agents</a>
        <a href="#" class="mx-2 hover:text-blue-600">Demos</a>
        <a href="#" class="mx-2 hover:text-blue-600">Case Studies</a>
      </nav>
    </header>

    <section class="text-center py-8 bg-gradient-to-r from-blue-50 to-blue-100">
      <h2 class="text-3xl font-semibold">Explore Next-Gen AI Agents</h2>
      <p class="text-gray-700">Interact, rate, and choose agents tailored for your healthcare needs.</p>
      <input type="text" id="agentSearch" placeholder="Search agents by category..." class="mt-4 p-2 w-1/3 rounded shadow border" oninput="searchAgents()">
    </section>

    <!-- Featured Agent Cards (2 columns) -->
    <section class="grid grid-cols-1 md:grid-cols-2 gap-4 p-8">
      <div class="agent-card bg-white rounded shadow-lg p-4" id="agent-1" data-keywords="diagnostics imaging">
        <img src="logo.png" alt="Company Logo" class="w-16 h-16 mb-2">
        <h4 class="font-bold text-xl">Sensely</h4>
        <p class="text-gray-600">AI-powered virtual assistant for medical triage.</p>
        <div class="my-3" id="feedback-agent-1"></div>
        <form onsubmit="submitFeedback(event, 'agent-1')">
          <div class="flex space-x-1 cursor-pointer" onclick="event.stopPropagation()">
            <svg xmlns="http://www.w3.org/2000/svg" class="star w-6 h-6" onclick="rateAgent(this.parentElement, 1)" fill="currentColor"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.286 3.957a1 1 0 00.95.69h4.163c.969 0 1.371 1.24.588 1.81l-3.37 2.448a1 1 0 00-.364 1.118l1.286 3.957c.3.921-.755 1.688-1.538 1.118l-3.37-2.448a1 1 0 00-1.175 0l-3.37 2.448c-.783.57-1.838-.197-1.538-1.118l1.286-3.957a1 1 0 00-.364-1.118L2.06 9.384c-.783-.57-.38-1.81.588-1.81h4.163a1 1 0 00.95-.69l1.286-3.957z"/></svg>
          </div>
          <input type="hidden" name="rating" value="0">
          <textarea name="review" placeholder="Write your review..." class="mt-2 p-2 border w-full rounded"></textarea>
          <button type="submit" class="mt-2 bg-blue-600 text-white px-3 py-1 rounded">Submit</button>
        </form>
        <a href="#" class="inline-block mt-2 text-blue-600 hover:underline">View Agent</a>
      </div>
      <!-- Add another featured agent card similarly -->
    </section>

    <!-- Other AI Agents (6 columns) -->
    <section class="grid grid-cols-2 md:grid-cols-6 gap-4 p-8">
      <!-- Repeat similar structure for additional agent cards -->
      <div class="agent-card bg-white rounded shadow-lg p-2" data-keywords="clinical decision support">
        <img src="logo.png" alt="Company Logo" class="w-12 h-12 mb-1">
        <h5 class="font-bold">Agent Name</h5>
      </div>
      <!-- Repeat for other agents -->
    </section>

    <footer class="bg-white text-center py-4 shadow">
      <p class="text-gray-600">© 2025 Synapster AI Marketplace</p>
    </footer>
  </div>
</body>
</html>
