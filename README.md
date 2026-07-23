import { motion } from "framer-motion";
import HeroTech from "./HeroTech";
import {
  fadeLeft,
  fadeUp,
  staggerContainer,
} from "../../animations/variants";

const HeroContent = () => {
  return (
    <motion.div
      variants={staggerContainer}
      initial="hidden"
      whileInView="visible"
      viewport={{ once: true, amount: 0.2 }}
      className="text-center lg:text-left"
    >
      {/* Badge */}
      <motion.div
        variants={fadeLeft}
        className="mb-6 inline-flex items-center gap-2 rounded-full border border-blue-500/30 bg-blue-500/10 px-4 py-2 text-xs font-medium text-blue-300 sm:text-sm"
      >
        👋 Hi, I'm
      </motion.div>

      {/* Main Heading */
      <motion.h1
        variants={fadeLeft}
        className="text-4xl font-extrabold leading-tight text-white sm:text-5xl lg:text-7xl"
      >
        Vivek Kadiyan
      </motion.h1>

      {/* Job Title */}
      <motion.h2
        variants={fadeLeft}
        className="mt-3 text-3xl font-bold sm:text-4xl lg:text-6xl"
      >
        <span className="bg-linear-to-r from-blue-500 to-cyan-400 bg-clip-text text-transparent">
          React.js
        </span>
        <span className="text-white"> Developer</span>
      </motion.h2>

      <motion.h2
        variants={fadeLeft}
        className="text-3xl font-bold text-white sm:text-4xl lg:text-6xl"
      >
        & Software Engineer
      </motion.h2>

      {/* Description */}
      <motion.p
        variants={fadeLeft}
        className="mx-auto mt-6 max-w-xl text-base leading-7 text-gray-400 sm:text-lg sm:leading-8 lg:mx-0"
      >
        4+ years of experience in building scalable web applications using
        React.js, TypeScript, ASP.NET Core and modern cloud technologies.
      </motion.p>

      {/* Buttons */}
      <motion.div
        variants={fadeUp}
        className="mt-10 flex flex-col gap-4 sm:flex-row sm:justify-center lg:justify-start"
      >
        <button className="w-full rounded-xl bg-linear-to-r from-blue-600 to-blue-500 px-8 py-4 font-semibold text-white transition-all duration-300 hover:-translate-y-1 hover:scale-105 hover:shadow-xl hover:shadow-blue-500/30 sm:w-auto">
          View My Work →
        </button>

        <button className="w-full rounded-xl border border-white/20 px-8 py-4 font-semibold text-white transition-all duration-300 hover:-translate-y-1 hover:border-blue-500 hover:bg-blue-500/10 sm:w-auto">
          Resume
        </button>
      </motion.div>

      {/* Tech Stack */}
      <motion.div
        variants={fadeUp}
        className="mt-12 flex justify-center lg:justify-start"
      >
        <HeroTech />
      </motion.div>
    </motion.div>
  );
};

export default HeroContent;
