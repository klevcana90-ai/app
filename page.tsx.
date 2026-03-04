"use client";

import { useState, useEffect } from "react";
import { useRouter } from "next/navigation";
import Link from "next/link";
import { 
  Sparkles, Zap, Target, TrendingUp, BarChart3, 
  Play, CheckCircle, ArrowRight, Menu, X, Star,
  Layers, Brain, Video, Gauge
} from "lucide-react";

export default function LandingPage() {
  const [mobileMenuOpen, setMobileMenuOpen] = useState(false);
  const [isLoggedIn, setIsLoggedIn] = useState(false);

  useEffect(() => {
    const token = localStorage.getItem("auth_token");
    if (token) {
      setIsLoggedIn(true);
    }
  }, []);

  const features = [
    {
      icon: <Sparkles className="w-7 h-7" />,
      title: "AI Ad Generator",
      description: "Generate complete ad packages with hooks, scripts, angles, and CTAs in seconds.",
      color: "from-indigo-500 to-purple-600"
    },
    {
      icon: <BarChart3 className="w-7 h-7" />,
      title: "Creative Analyzer",
      description: "Analyze scripts for hook strength, emotional triggers, and conversion potential.",
      color: "from-emerald-500 to-teal-600"
    },
    {
      icon: <Layers className="w-7 h-7" />,
      title: "Variation Engine",
      description: "Instantly create multiple ad variations for A/B testing across platforms.",
      color: "from-orange-500 to-red-500"
    },
    {
      icon: <Brain className="w-7 h-7" />,
      title: "Retention Psychology",
      description: "Optimized script structure to maximize watch time and engagement.",
      color: "from-violet-500 to-purple-600"
    },
    {
      icon: <Target className="w-7 h-7" />,
      title: "Platform Optimization",
      description: "Tailored outputs for TikTok, Instagram Reels, Facebook, and YouTube Shorts.",
      color: "from-blue-500 to-cyan-600"
    },
    {
      icon: <Video className="w-7 h-7" />,
      title: "Shot-by-Shot Guide",
      description: "Step-by-step filming instructions with visual cues and subtitle guidance.",
      color: "from-pink-500 to-rose-600"
    }
  ];

  const testimonials = [
    {
      name: "Sarah Chen",
      role: "Performance Marketing Lead",
      company: "GlowBeauty",
      image: "https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=100&h=100&fit=crop",
      text: "CreativeOS cut our ad creation time from 6 hours to 15 minutes. We're now testing 3x more creatives.",
      rating: 5
    },
    {
      name: "Marcus Johnson",
      role: "Founder & CEO",
      company: "FitGear Pro",
      image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=100&h=100&fit=crop",
      text: "The Creative Analyzer is a game-changer. It's like having a $10k/month strategist reviewing every script.",
      rating: 5
    },
    {
      name: "Emily Rodriguez",
      role: "Media Buyer",
      company: "ScaleUp Agency",
      image: "https://images.unsplash.com/photo-1438761681033-6461ffad8d80?w=100&h=100&fit=crop",
      text: "We scaled our clients from $50k to $500k/month using CreativeOS. Absolute lifesaver.",
      rating: 5
    }
  ];

  const plans = [
    { name: "Starter", price: 29, generations: "30 generations/month", features: ["AI Ad Generator", "Creative Analyzer", "Email Support"], popular: false },
    { name: "Pro", price: 59, generations: "150 generations/month", features: ["Everything in Starter", "Ad Variation Engine", "Priority Support"], popular: true },
    { name: "Scale", price: 129, generations: "Unlimited", features: ["Everything in Pro", "White Label", "API Access"], popular: false }
  ];

  return (
    <div className="min-h-screen bg-white">
      {/* 1. Navbar */}
      <header className="fixed top-0 w-full z-50 bg-white/80 backdrop-blur-xl border-b border-slate-100">
        <div className="max-w-[1280px] mx-auto px-6 lg:px-8">
          <div className="flex items-center justify-between h-20">
            <Link href="/" className="flex items-center gap-3">
              <div className="w-10 h-10 bg-gradient-to-br from-indigo-600 to-purple-600 rounded-xl flex items-center justify-center">
                <Zap className="w-5 h-5 text-white" />
              </div>
              <span className="font-bold text-2xl text-slate-900">CreativeOS</span>
            </Link>

            <nav className="hidden md:flex items-center gap-8 ml-auto">
              <a href="#features" className="text-slate-600 hover:text-indigo-600 font-semibold transition-colors">Features</a>
              <a href="#testimonials" className="text-slate-600 hover:text-indigo-600 font-semibold transition-colors">Testimonials</a>
              <a href="#pricing" className="text-slate-600 hover:text-indigo-600 font-semibold transition-colors">Pricing</a>
              <div className="h-6 w-[1px] bg-slate-200 mx-2"></div>
              {isLoggedIn ? (
                <Link href="/dashboard" className="px-6 py-2.5 bg-indigo-600 text-white font-bold rounded-full">Dashboard</Link>
              ) : (
                <>
                  <Link href="/login" className="text-slate-600 font-semibold">Log in</Link>
                  <Link href="/register" className="px-6 py-2.5 bg-indigo-600 text-white font-bold rounded-full hover:bg-indigo-700 transition-all">
                    Start Free Trial
                  </Link>
                </>
              )}
            </nav>

            <button className="md:hidden" onClick={() => setMobileMenuOpen(!mobileMenuOpen)}>
              {mobileMenuOpen ? <X /> : <Menu />}
            </button>
          </div>
        </div>
      </header>

      {/* 2. Hero Section */}
      <section className="relative pt-40 pb-24 lg:pt-56 overflow-hidden">
        <div className="absolute top-0 left-1/2 -translate-x-1/2 w-full h-full -z-10">
          <div className="absolute top-[-10%] left-[-10%] w-[40%] h-[40%] bg-indigo-50 rounded-full blur-[120px] opacity-60"></div>
          <div className="absolute bottom-[-10%] right-[-10%] w-[30%] h-[30%] bg-purple-50 rounded-full blur-[100px] opacity-60"></div>
        </div>

        <div className="max-w-[1280px] mx-auto px-6 lg:px-8">
          <div className="text-center max-w-4xl mx-auto mb-16">
            <h1 className="text-5xl lg:text-7xl font-black text-slate-900 tracking-tight leading-[1.1] mb-8">
              Build, Test & Scale <br/>
              <span className="text-transparent bg-clip-text bg-gradient-to-r from-indigo-600 to-purple-600">Winning Ads</span> — Automatically
            </h1>
            <p className="text-xl lg:text-2xl font-medium text-slate-600 mb-10">
              The AI Content Engine for High-Performance Media Buyers.
            </p>
            
            <div className="flex flex-col sm:flex-row items-center justify-center gap-6">
              <Link href="/register" className="w-full sm:w-auto px-10 py-5 bg-indigo-600 text-white text-lg font-bold rounded-2xl shadow-xl hover:bg-indigo-700 transition-all transform hover:scale-105 flex items-center justify-center gap-2">
                <Sparkles className="w-5 h-5" /> Start Free Trial
              </Link>
              <div className="flex gap-4 text-sm font-bold text-slate-500">
                <span className="flex items-center gap-1"><CheckCircle className="w-4 h-4 text-emerald-500"/> No Credit Card</span>
                <span className="flex items-center gap-1"><CheckCircle className="w-4 h-4 text-emerald-500"/> 3 Free Ads</span>
              </div>
            </div>
          </div>

          {/* Video Proof Container */}
          <div className="relative max-w-5xl mx-auto">
            <div className="absolute -inset-2 bg-gradient-to-r from-indigo-500 to-purple-600 rounded-3xl blur opacity-15"></div>
            <div className="relative aspect-video bg-slate-900 rounded-2xl shadow-2xl overflow-hidden border border-slate-200">
              <iframe
                className="absolute inset-0 w-full h-full"
                src="https://www.youtube.com/embed/8AyVh1_vWYQ?rel=0"
                title="CreativeOS Demo"
                frameBorder="0"
                allowFullScreen
              ></iframe>
            </div>
          </div>
        </div>
      </section>

      {/* 3. Features Section */}
      <section id="features" className="py-24 bg-slate-50">
        <div className="max-w-[1280px] mx-auto px-8">
          <div className="text-center mb-16">
            <h2 className="text-4xl lg:text-5xl font-bold mb-6">Everything You Need to Create <span className="text-indigo-600">Winning Ads</span></h2>
            <p className="text-xl text-slate-600 max-w-2xl mx-auto">The complete creative suite for performance marketers.</p>
          </div>
          <div className="grid grid-cols-1 md:grid-cols-3 gap-10">
            {features.map((f, i) => (
              <div key={i} className="bg-white p-8 rounded-2xl border border-slate-200 hover:shadow-xl transition-all">
                <div className={`w-12 h-12 bg-gradient-to-br ${f.color} rounded-lg mb-6 flex items-center justify-center text-white`}>
                  {f.icon}
                </div>
                <h3 className="text-xl font-bold mb-3">{f.title}</h3>
                <p className="text-slate-600">{f.description}</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="py-12 bg-white border-t border-slate-100 text-center">
        <p className="text-slate-500">© 2026 CreativeOS. The #1 AI Ad Generator for Shopify Brands.</p>
      </footer>
    </div>
  );
}
