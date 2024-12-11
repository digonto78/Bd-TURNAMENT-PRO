// script.js
document.getElementById("registrationForm").addEventListener("submit", function(e) {
    e.preventDefault(); // ফর্ম সাবমিট আটকানো
    const name = document.getElementById("name").value;
    const email = document.getElementById("email").value;

    if (name && email) {
        // অংশগ্রহণকারীর তালিকায় যোগ করা
        const participantList = document.getElementById("participantList");
        const li = document.createElement("li");
        li.textContent = `${name} (${email})`;
        participantList.appendChild(li);

        // ফর্ম রিসেট করা
        document.getElementById("registrationForm").reset();
    }
});