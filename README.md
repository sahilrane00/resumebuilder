import React, { useState } from "react";

export default function ResumeBuilder() {
  const [formData, setFormData] = useState({
    name: "",
    email: "",
    phone: "",
    address: "",
    education: "",
    experience: "",
    skills: "",
  });

  const handleChange = (e) => {
    setFormData({ ...formData, [e.target.name]: e.target.value });
  };

  return (
    <div className="p-6 max-w-3xl mx-auto bg-white rounded-lg shadow-lg">
      <h2 className="text-xl font-bold mb-4">Online Resume Builder</h2>

      <input
        type="text"
        name="name"
        placeholder="Full Name"
        value={formData.name}
        onChange={handleChange}
        className="w-full p-2 mb-2 border rounded"
      />
      <input
        type="email"
        name="email"
        placeholder="Email"
        value={formData.email}
        onChange={handleChange}
        className="w-full p-2 mb-2 border rounded"
      />
      <input
        type="text"
        name="phone"
        placeholder="Phone Number"
        value={formData.phone}
        onChange={handleChange}
        className="w-full p-2 mb-2 border rounded"
      />
      <textarea
        name="address"
        placeholder="Address"
        value={formData.address}
        onChange={handleChange}
        className="w-full p-2 mb-2 border rounded"
      />
      <textarea
        name="education"
        placeholder="Education"
        value={formData.education}
        onChange={handleChange}
        className="w-full p-2 mb-2 border rounded"
      />
      <textarea
        name="experience"
        placeholder="Work Experience"
        value={formData.experience}
        onChange={handleChange}
        className="w-full p-2 mb-2 border rounded"
      />
      <textarea
        name="skills"
        placeholder="Skills"
        value={formData.skills}
        onChange={handleChange}
        className="w-full p-2 mb-4 border rounded"
      />

      <button
        onClick={() => console.log("Resume Data:", formData)}
        className="bg-blue-500 text-white px-4 py-2 rounded"
      >
        Generate Resume
      </button>
    </div>
  );
}
