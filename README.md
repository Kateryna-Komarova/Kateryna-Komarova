import React, { useState, useEffect } from 'react';
import { Terminal, Code2, Bug, Coffee, Brain, Rocket, Book, Award } from 'lucide-react';

const AnimatedProfile = () => {
  const [isVisible, setIsVisible] = useState(false);
  
  useEffect(() => {
    setIsVisible(true);
  }, []);

  const skills = {
    manual_testing: ["Test Cases", "Bug Reports", "Test Strategy"],
    automation: ["Selenium", "TestNG", "Cucumber", "JUnit"],
    api_testing: ["Postman", "REST", "SOAP", "Swagger"],
    databases: ["MySQL", "MongoDB"],
    tools: ["Jenkins", "Git", "JIRA", "TestRail"]
  };

  return (
    <div className="w-full max-w-4xl mx-auto p-8 space-y-8">
      {/* Hero Section with Animated Title */}
      <div className="relative overflow-hidden rounded-lg bg-gradient-to-r from-purple-600 to-blue-600 p-8 text-white">
        <div className={`transform transition-all duration-1000 ${isVisible ? 'translate-y-0 opacity-100' : 'translate-y-10 opacity-0'}`}>
          <h1 className="text-4xl font-bold mb-4">⚡ Quality Assurance Engineer ⚡</h1>
          <p className="text-xl font-light">"Testing leads to failure, and failure leads to understanding" - Burt Rutan</p>
          <div className="mt-4 flex space-x-4">
            <Terminal className="animate-bounce" />
            <Code2 className="animate-pulse" />
            <Bug className="animate-spin-slow" />
          </div>
        </div>
      </div>

      {/* Skills Grid */}
      <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
        {Object.entries(skills).map(([category, items], index) => (
          <div
            key={category}
            className={`bg-white p-6 rounded-lg shadow-lg transform transition-all duration-500 hover:scale-105 ${
              isVisible ? 'translate-y-0 opacity-100' : 'translate-y-10 opacity-0'
            }`}
            style={{ transitionDelay: `${index * 200}ms` }}
          >
            <h3 className="text-lg font-bold mb-3 text-purple-600 capitalize">
              {category.replace('_', ' ')}
            </h3>
            <div className="flex flex-wrap gap-2">
              {items.map((item, i) => (
                <span
                  key={i}
                  className="px-3 py-1 bg-gray-100 rounded-full text-sm font-medium hover:bg-purple-100 transition-colors"
                >
                  {item}
                </span>
              ))}
            </div>
          </div>
        ))}
      </div>

      {/* Tech Stack */}
      <div className={`bg-white p-6 rounded-lg shadow-lg transform transition-all duration-500 ${
        isVisible ? 'translate-y-0 opacity-100' : 'translate-y-10 opacity-0'
      }`}>
        <h2 className="text-2xl font-bold mb-6 text-center">🛠 Tech Stack</h2>
        <div className="space-y-6">
          <div className="space-y-4">
            <h3 className="text-lg font-semibold">🔧 Testing Tools & Frameworks</h3>
            <div className="flex flex-wrap gap-4">
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">Selenium</div>
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">Postman</div>
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">Jenkins</div>
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">Docker</div>
            </div>
          </div>
          
          <div className="space-y-4">
            <h3 className="text-lg font-semibold">💻 Programming & Development</h3>
            <div className="flex flex-wrap gap-4">
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">Java</div>
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">HTML</div>
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">CSS</div>
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">JavaScript</div>
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">Git</div>
            </div>
          </div>

          <div className="space-y-4">
            <h3 className="text-lg font-semibold">🗄️ Databases & Tools</h3>
            <div className="flex flex-wrap gap-4">
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">MySQL</div>
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">MongoDB</div>
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">GitHub</div>
              <div className="p-4 bg-gray-50 rounded-lg hover:bg-purple-50 transition-colors">IntelliJ IDEA</div>
            </div>
          </div>
        </div>
      </div>

      {/* Footer Quote */}
      <div className="text-center mt-8">
        <p className="text-lg font-medium text-purple-600 animate-pulse">
          "Making the digital world a better place, one test at a time! 🚀"
        </p>
      </div>
    </div>
  );
};

export default AnimatedProfile;
<!---
Kateryna-Komarova/Kateryna-Komarova is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
