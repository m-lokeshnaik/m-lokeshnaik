import React from 'react';
import { Github, Linkedin, Instagram, Mail, ExternalLink, Code, Database, Cpu, Globe } from 'lucide-react';
import { Card, CardContent } from '@/components/ui/card';
import { Badge } from '@/components/ui/badge';
import { Button } from '@/components/ui/button';

const Index = () => {
  const socialLinks = [
    {
      name: 'GitHub',
      url: 'https://github.com/m-lokeshnaik',
      icon: <Github className="w-5 h-5" />,
      color: 'hover:bg-gray-800'
    },
    {
      name: 'LinkedIn',
      url: 'https://www.linkedin.com/in/lokesh-naik-0a7a27257',
      icon: <Linkedin className="w-5 h-5" />,
      color: 'hover:bg-blue-600'
    },
    {
      name: 'Instagram',
      url: 'https://www.instagram.com/_unknown_user7569/',
      icon: <Instagram className="w-5 h-5" />,
      color: 'hover:bg-pink-600'
    },
    {
      name: 'Email',
      url: 'mailto:lokeshnaik7569@gmail.com',
      icon: <Mail className="w-5 h-5" />,
      color: 'hover:bg-red-600'
    }
  ];

  const programmingLanguages = [
    { name: 'Python', color: 'bg-blue-500' },
    { name: 'C', color: 'bg-blue-600' },
    { name: 'SQL', color: 'bg-orange-500' },
    { name: 'HTML', color: 'bg-orange-600' },
    { name: 'CSS', color: 'bg-blue-400' },
    { name: 'Bash', color: 'bg-gray-700' }
  ];

  const frameworks = [
    { name: 'TensorFlow', color: 'bg-orange-500' },
    { name: 'PyTorch', color: 'bg-red-500' },
    { name: 'Keras', color: 'bg-red-600' },
    { name: 'OpenCV', color: 'bg-green-600' },
    { name: 'NumPy', color: 'bg-blue-700' },
    { name: 'Pandas', color: 'bg-purple-600' },
    { name: 'Arduino', color: 'bg-teal-600' }
  ];

  const tools = [
    { name: 'Git', color: 'bg-orange-600' },
    { name: 'Jupyter', color: 'bg-orange-500' },
    { name: 'VS Code', color: 'bg-blue-600' },
    { name: 'Google Colab', color: 'bg-yellow-500' },
    { name: 'Kaggle', color: 'bg-blue-400' },
    { name: 'MySQL', color: 'bg-blue-600' }
  ];

  const achievements = [
    "Senior ML Engineering Student",
    "3D Model Designer",
    "Machine Learning Engineer",
    "Problem Solver on HackerRank & LeetCode"
  ];

  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-50 via-blue-50 to-indigo-100">
      {/* Header Section */}
      <div className="relative overflow-hidden bg-gradient-to-r from-blue-600 via-purple-600 to-indigo-600 text-white">
        <div className="absolute inset-0 bg-black/20"></div>
        <div className="relative max-w-6xl mx-auto px-6 py-16">
          <div className="text-center">
            <div className="mb-6">
              <div className="w-32 h-32 mx-auto bg-white/20 rounded-full flex items-center justify-center mb-4 backdrop-blur-sm">
                <span className="text-4xl font-bold">LN</span>
              </div>
              <h1 className="text-5xl font-bold mb-2">
                Lokesh Naik
                <span className="inline-block ml-2 animate-bounce">👋</span>
              </h1>
              <p className="text-xl text-blue-100 mb-6">Machine Learning Engineer & 3D Model Designer</p>
            </div>
            <div className="flex justify-center space-x-4 mb-8">
              {socialLinks.map((link) => (
                <a
                  key={link.name}
                  href={link.url}
                  target="_blank"
                  rel="noopener noreferrer"
                  className={`p-3 bg-white/20 backdrop-blur-sm rounded-full transition-all duration-300 ${link.color} transform hover:scale-110`}
                >
                  {link.icon}
                </a>
              ))}
            </div>
            <div className="flex justify-center space-x-4">
              <Button variant="secondary" className="bg-white/20 backdrop-blur-sm border-white/30 text-white hover:bg-white/30">
                <a href="https://drive.google.com/file/d/19qUDTip3cK46cOTUqWOatk1VmC9FnC8l/view?usp=drive_link" target="_blank" rel="noopener noreferrer" className="flex items-center">
                  View Resume <ExternalLink className="ml-2 w-4 h-4" />
                </a>
              </Button>
            </div>
          </div>
        </div>
      </div>
      {/* Main Content */}
      <div className="max-w-6xl mx-auto px-6 py-12">
        {/* About Section */}
        <Card className="mb-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
          <CardContent className="p-8">
            <h2 className="text-3xl font-bold mb-6 text-gray-800 flex items-center">
              <Code className="mr-3 text-blue-600" />
              About Me
            </h2>
            <div className="grid md:grid-cols-2 gap-8">
              <div>
                <p className="text-gray-600 text-lg leading-relaxed mb-6">
                  I am a machine learning engineer and 3D model designer who loves programming, reading, writing and speaking. 
                  As a ML engineer, I enjoy using my obsessive attention to detail and my unequivocal love for making things that change the world.
                </p>
                <p className="text-gray-600 text-lg leading-relaxed">
                  That's why I like to make things that make a difference.
                </p>
              </div>
              <div>
                <h3 className="text-xl font-semibold mb-4 text-gray-800">Achievements</h3>
                <div className="space-y-3">
                  {achievements.map((achievement, index) => (
                    <div key={index} className="flex items-center">
                      <div className="w-2 h-2 bg-blue-600 rounded-full mr-3"></div>
                      <span className="text-gray-600">{achievement}</span>
                    </div>
                  ))}
                </div>
              </div>
            </div>
          </CardContent>
        </Card>
        {/* Current Learning */}
        <Card className="mb-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
          <CardContent className="p-8">
            <h2 className="text-3xl font-bold mb-6 text-gray-800 flex items-center">
              <Cpu className="mr-3 text-green-600" />
              Currently Learning
            </h2>
            <div className="grid md:grid-cols-2 gap-6">
              <div className="bg-gradient-to-r from-blue-50 to-indigo-50 p-6 rounded-lg">
                <h3 className="text-lg font-semibold mb-3 text-gray-800">Data Structures & Algorithms</h3>
                <p className="text-gray-600 mb-3">Practicing on HackerRank to strengthen problem-solving skills</p>
                <a href="https://www.hackerrank.com/lokeshnaik7569" target="_blank" rel="noopener noreferrer" className="text-blue-600 hover:text-blue-800 flex items-center">
                  View Profile <ExternalLink className="ml-2 w-4 h-4" />
                </a>
              </div>
              <div className="bg-gradient-to-r from-orange-50 to-red-50 p-6 rounded-lg">
                <h3 className="text-lg font-semibold mb-3 text-gray-800">TensorFlow Ecosystem</h3>
                <p className="text-gray-600">Exploring advanced tools and technologies for machine learning</p>
              </div>
            </div>
          </CardContent>
        </Card>
        {/* Skills Section */}
        <div className="grid lg:grid-cols-3 gap-8 mb-8">
          <Card className="shadow-lg hover:shadow-xl transition-shadow duration-300">
            <CardContent className="p-6">
              <h3 className="text-xl font-bold mb-4 text-gray-800 flex items-center">
                <Code className="mr-2 text-blue-600" />
                Programming Languages
              </h3>
              <div className="flex flex-wrap gap-2">
                {programmingLanguages.map((lang) => (
                  <Badge key={lang.name} className={`${lang.color} text-white hover:scale-105 transition-transform`}>
                    {lang.name}
                  </Badge>
                ))}
              </div>
            </CardContent>
          </Card>
          <Card className="shadow-lg hover:shadow-xl transition-shadow duration-300">
            <CardContent className="p-6">
              <h3 className="text-xl font-bold mb-4 text-gray-800 flex items-center">
                <Cpu className="mr-2 text-green-600" />
                Frameworks & Libraries
              </h3>
              <div className="flex flex-wrap gap-2">
                {frameworks.map((framework) => (
                  <Badge key={framework.name} className={`${framework.color} text-white hover:scale-105 transition-transform`}>
                    {framework.name}
                  </Badge>
                ))}
              </div>
            </CardContent>
          </Card>
          <Card className="shadow-lg hover:shadow-xl transition-shadow duration-300">
            <CardContent className="p-6">
              <h3 className="text-xl font-bold mb-4 text-gray-800 flex items-center">
                <Database className="mr-2 text-purple-600" />
                Tools & Software
              </h3>
              <div className="flex flex-wrap gap-2">
                {tools.map((tool) => (
                  <Badge key={tool.name} className={${tool.color} text-white hover:scale-105 transition-transform}>
                    {tool.name}
                  </Badge>
                ))}
              </div>
            </CardContent>
          </Card>
        </div>
        {/* Coding Platforms */}
        <Card className="shadow-lg hover:shadow-xl transition-shadow duration-300">
          <CardContent className="p-8">
            <h2 className="text-3xl font-bold mb-6 text-gray-800 flex items-center">
              <Globe className="mr-3 text-indigo-600" />
              Coding Platforms
            </h2>
            <div className="grid md:grid-cols-3 gap-6">
              <a href="https://github.com/m-lokeshnaik" target="_blank" rel="noopener noreferrer" className="block">
                <div className="bg-gradient-to-r from-gray-800 to-black text-white p-6 rounded-lg hover:scale-105 transition-transform">
                  <Github className="w-8 h-8 mb-3" />
                  <h3 className="text-lg font-semibold">GitHub</h3>
                  <p className="text-gray-300">View my repositories and projects</p>
                </div>
              </a>
              <a href="https://leetcode.com/lokeshnaik7569/" target="_blank" rel="noopener noreferrer" className="block">
                <div className="bg-gradient-to-r from-orange-500 to-yellow-500 text-white p-6 rounded-lg hover:scale-105 transition-transform">
                  <Code className="w-8 h-8 mb-3" />
                  <h3 className="text-lg font-semibold">LeetCode</h3>
                  <p className="text-orange-100">Algorithm problem solving</p>
                </div>
              </a>
              <a href="https://www.hackerrank.com/lokeshnaik7569" target="_blank" rel="noopener noreferrer" className="block">
                <div className="bg-gradient-to-r from-green-500 to-teal-500 text-white p-6 rounded-lg hover:scale-105 transition-transform">
                  <Database className="w-8 h-8 mb-3" />
                  <h3 className="text-lg font-semibold">HackerRank</h3>
                  <p className="text-green-100">Coding challenges and contests</p>
                </div>
              </a>
            </div>
          </CardContent>
        </Card>
        {/* Contact Section */}
        <div className="text-center mt-12 p-8 bg-gradient-to-r from-blue-600 to-purple-600 rounded-lg text-white">
          <h2 className="text-2xl font-bold mb-4">Let's Connect!</h2>
          <p className="text-lg mb-6">Feel free to reach out for collaborations or just a friendly chat</p>
          <a href="mailto:lokeshnaik7569@gmail.com" className="inline-flex items-center bg-white text-blue-600 px-6 py-3 rounded-full font-semibold hover:bg-blue-50 transition-colors">
            <Mail className="mr-2 w-5 h-5" />
            lokeshnaik7569@gmail.com
          </a>
        </div>
      </div>
    </div>
  );
};

export default Index;
