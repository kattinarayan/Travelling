function scrollToDemo() {
  document.getElementById("demo").scrollIntoView({ behavior: "smooth" });
}

function generatePlan() {
  const city = document.getElementById("city").value;
  const days = document.getElementById("days").value;
  const budget = document.getElementById("budget").value;

  if (!city || !days || !budget) {
    alert("Please select all fields");
    return;
  }

  const output = document.getElementById("output");

  output.innerHTML = `
    <h3>Sample Trip Plan</h3>
    <p><strong>City:</strong> ${city.toUpperCase()}</p>
    <p><strong>Days:</strong> ${days}</p>
    <p><strong>Budget:</strong> ${budget}</p>
    <hr>
    <p>9:00 AM – Local Temple (Free)</p>
    <p>11:00 AM – Waterfall (₹30)</p>
    <p>2:00 PM – Lunch (₹150)</p>
    <p>4:30 PM – Viewpoint (Free)</p>
    <hr>
    <small>*This is a demo preview, not a real plan</small>
  `;
}
