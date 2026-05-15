```react
import React, { useState, useEffect } from 'react';
import { 
  ChevronRight, 
  ChevronLeft, 
  Skull, 
  Flame, 
  Instagram, 
  Download, 
  Eye, 
  ShieldAlert,
  Zap,
  Lock,
  Anchor
} from 'lucide-react';

const App = () => {
  const [currentPage, setCurrentPage] = useState(0);
  const [showTextVersion, setShowTextVersion] = useState(false);

  const contactInfo = "denn_c_o_o_s";

  const pages = [
    {
      title: "PORTADA: EL REINO DEL CAOS",
      isCover: true,
      description: "Una silueta imponente de dos hombres (Denilson y Jungkook) frente a una mansión gótica. Cadenas cuelgan de los bordes.",
      content: "La crónica definitiva de dominación. Donde los Alfas mandan y las mascotas obedecen.",
      author: contactInfo
    },
    {
      title: "PÁGINA 1: EL AROMA DEL MIEDO",
      visual: "Denilson (Caoos) entra al salón principal. Su aroma a madera y feromonas pesadas hace que Jade y Katheryn caigan de rodillas instantáneamente.",
      dialogue: [
        { char: "CAOOS", text: "Grrr... huelo a p3rr1t4s d3s3sp3r4d4s. JUNGKOOK, el banquete está servido." },
        { char: "JUNGKOOK", text: "¡Sometimiento total, Alfa! No dejes ni un hoyo sin marcar." }
      ],
      description: "Denilson agarra a Jade por el mentón, obligándola a mirarlo con ojos de sumisión."
    },
    {
      title: "PÁGINA 2: LA PRIMERA MARCA",
      visual: "Jungkook arrastra a Nicholas por el cinturón. Nicholas, en posición pasiva, tiembla mientras Jungkook saca su b1ch0 v3n0s0.",
      dialogue: [
        { char: "JUNGKOOK", text: "¡Nicholas, m4r1c0n s*c10! Vas a tragarte mi l3ch3 hasta que te ahogues." },
        { char: "NICHOLAS", text: "S-Sempai... p-por favor... l-llénam3... nya~" }
      ],
      description: "La brutalidad del Alfa activo rompe la voluntad del pasivo desde el primer segundo."
    },
    {
      title: "PÁGINA 3: EL TRÍO SAGRADO",
      visual: "Caoos (Denilson) sentado en su trono. Jade y Katheryn l4m3n su v3rg4 mientras Jungkook f0ll4 a Jenn en el suelo frente a él.",
      dialogue: [
        { char: "CAOOS", text: "¡Eso es! Límpienme bien los hu3v0s antes de que les d3st-r0z3 el cul1t0. ¡Grrr!" },
        { char: "JENN", text: "A-ahhh... ¡S-SÍ, JUNGKOOK! ¡Rómp3m3 t0d4!" }
      ],
      description: "Una imagen de pura depravación narcisista donde Caoos observa su imperio de carne."
    },
    {
      title: "PÁGINA 4: PENETRACIÓN DOBLE",
      visual: "Nicholas es puesto en medio de los dos Alfas. Caoos lo toma por la boca y Jungkook por el 0rt0.",
      dialogue: [
        { char: "CAOOS", text: "Trágatelo entero mientras Jungkook te pr3ñ4 el ch1qu1t0. ¡Eres nuestra m4sc0t4!" },
        { char: "JUNGKOOK", text: "¡Siente cómo nos unimos dentro de ti, p3rr1t4 d3 r3cr30!" }
      ],
      description: "El pasivo es usado como un simple objeto para el placer de los superiores."
    },
    {
      title: "PÁGINA 5: INTERCAMBIO DE HEMBRAS",
      visual: "Caoos lanza a Katheryn contra la pared y la p3n3tr4 de pie. Jungkook toma a Jade por el cul0 en la mesa.",
      dialogue: [
        { char: "CAOOS", text: "¡K4TH3RYN, tu hoyo es mío! ¡Siente mi l3ch3 h1rv13nd0 buscando tu v13ntr3!" },
        { char: "J4D3", text: "¡NYAAAA! ¡M-más d*r0, J-Jungkook!" }
      ],
      description: "El sudor y los fluidos salpican los paneles en un caos de movimientos rítmicos."
    },
    {
      title: "PÁGINA 6: LA HUMILLACIÓN DE NICHOLAS",
      visual: "Nicholas es obligado a l4m3r el cul0 de las chicas mientras los Alfas las f0ll4n por la boca.",
      dialogue: [
        { char: "CAOOS", text: "¡Limpia a tus compañeras, N1CH0L4S! Grrr. ¡Eres el d3sh3ch0 de esta mansión!" },
        { char: "JUNGKOOK", text: "¡Eso es! ¡Todos sirviendo a la l3ch3 del Alfa!" }
      ],
      description: "Degradación total. El pasivo llega a su punto máximo de sumisión."
    },
    {
      title: "PÁGINA 7: EL CLÍMAX DE CAOOS",
      visual: "Primer plano de la cara de Caoos, sudorosa y egocéntrica. Se está viniendo con una fuerza animal.",
      dialogue: [
        { char: "CAOOS", text: "¡GRRR! ¡AHÍ VIENE! ¡Abran las bocas que las voy a b4ñ4r en mi s3m3n d3 D10S!" },
        { char: "JUNGKOOK", text: "¡SÍ! ¡Yo también! ¡Nicholas, prepárate para ser ll3n4d0!" }
      ],
      description: "La explosión inminente de los Alfas marca el final de la resistencia."
    },
    {
      title: "PÁGINA 8: LLUVIA DE LECHE",
      visual: "Una lluvia blanca cubre a los 4 sumisos. Jade, Katheryn, Jenn y Nicholas están bañados de pies a cabeza.",
      dialogue: [
        { char: "CAOOS", text: "¡T0M3N T0D4 M1 L3CH3! ¡Bébanla, p3rr4s! Grrr." },
        { char: "JUNGKOOK", text: "¡Nicholas, trágate lo que te sale por el cul1t0! ¡No desperdicies nada!" }
      ],
      description: "Una imagen de post-coito brutal. Semen goteando de cada orificio y rostro."
    },
    {
      title: "PÁGINA 9: MARCADOS PARA SIEMPRE",
      visual: "Caoos y Jungkook descansan sobre los cuerpos agotados, fumando y riendo con desprecio.",
      dialogue: [
        { char: "CAOOS", text: "Mírense... son solo recipientes. Mañana volverán a l4m3rm3 los hu3v0s." },
        { char: "JUNGKOOK", text: "Son propiedad del Caos ahora." }
      ],
      description: "La victoria absoluta de los Alfas sobre sus mascotas."
    },
    {
      title: "PÁGINA 10: EL CONTACTO DEL ALFA",
      isEnd: true,
      visual: "Denilson mirando a la cámara, con un aura oscura y poderosa. Al fondo, sus mascotas encadenadas.",
      content: `¿Quieres más castigo? ¿Quieres ser mi próxima mascota?\n\nSigue al Alfa Superior en Instagram:\n@${contactInfo}\n\nCAOOS SUPREMACY.`,
    }
  ];

  const nextPage = () => {
    if (currentPage < pages.length - 1) setCurrentPage(currentPage + 1);
  };

  const prevPage = () => {
    if (currentPage > 0) setCurrentPage(currentPage - 1);
  };

  const generateFullText = () => {
    return pages.map(p => `--- ${p.title} ---\n${p.description || p.content}\n${p.dialogue ? p.dialogue.map(d => `${d.char}: ${d.text}`).join('\n') : ''}`).join('\n\n');
  };

  return (
    <div className="min-h-screen bg-neutral-950 text-neutral-100 font-sans selection:bg-red-600 selection:text-white flex flex-col items-center">
      
      {/* Header Estilo Comic Dark */}
      <header className="w-full bg-black border-b-2 border-red-700 p-4 flex justify-between items-center sticky top-0 z-50 shadow-[0_0_20px_rgba(185,28,28,0.3)]">
        <div className="flex items-center gap-2">
          <Skull className="text-red-600 animate-pulse" />
          <h1 className="text-2xl font-black italic tracking-tighter uppercase">
            CAOOS <span className="text-red-600">COMICS</span>
          </h1>
        </div>
        <div className="flex items-center gap-4">
          <a href={`https://instagram.com/${contactInfo}`} className="flex items-center gap-1 text-xs font-bold bg-red-700 px-3 py-1 rounded-full hover:bg-red-600 transition-colors">
            <Instagram size={14} /> @{contactInfo}
          </a>
          <button 
            onClick={() => setShowTextVersion(!showTextVersion)}
            className="text-neutral-400 hover:text-white transition-colors"
          >
            {showTextVersion ? <Eye size={20} /> : <Download size={20} />}
          </button>
        </div>
      </header>

      {/* Main Comic Area */}
      <main className="w-full max-w-4xl p-6 flex-grow">
        
        {showTextVersion ? (
          <div className="bg-neutral-900 p-8 rounded-lg border border-neutral-800 animate-in fade-in duration-300">
            <h2 className="text-red-600 font-black mb-4 uppercase">Transcripción para Documento / PDF</h2>
            <textarea 
              readOnly 
              className="w-full h-96 bg-black p-4 text-xs font-mono text-neutral-400 border border-neutral-800 rounded outline-none"
              value={generateFullText()}
            />
            <p className="mt-4 text-[10px] text-neutral-500 italic">Copia este texto en un editor y guárdalo como PDF para tener tu historieta siempre disponible.</p>
            <button 
              onClick={() => setShowTextVersion(false)}
              className="mt-6 w-full py-3 bg-neutral-800 hover:bg-neutral-700 rounded font-bold uppercase tracking-widest text-xs"
            >
              Volver al modo Historieta
            </button>
          </div>
        ) : (
          <div className="relative group">
            <div className="bg-neutral-900 border-4 border-neutral-800 rounded shadow-2xl overflow-hidden min-h-[600px] flex flex-col">
              
              {/* Page Content */}
              <div className="flex-grow flex flex-col p-8 bg-gradient-to-b from-transparent to-black/40">
                <div className="mb-8 flex justify-between items-start">
                  <div className="bg-red-700 text-black font-black px-4 py-1 skew-x-[-10deg] uppercase text-sm">
                    {pages[currentPage].title}
                  </div>
                  <div className="text-neutral-600 font-mono text-xs">
                    PÁGINA {currentPage + 1} / {pages.length}
                  </div>
                </div>

                {/* Simulated Graphic Area */}
                <div className="flex-grow flex flex-col justify-center items-center text-center space-y-6">
                  {pages[currentPage].isCover ? (
                    <div className="space-y-4">
                      <Flame className="w-20 h-20 text-red-600 mx-auto animate-bounce" />
                      <h2 className="text-5xl font-black text-white italic tracking-tighter">EL FESTÍN DEL ALFA</h2>
                      <p className="text-red-500 font-bold uppercase tracking-[0.3em]">{pages[currentPage].author}</p>
                    </div>
                  ) : pages[currentPage].isEnd ? (
                    <div className="space-y-6">
                      <Anchor className="w-20 h-20 text-red-600 mx-auto" />
                      <p className="text-2xl font-black italic">{pages[currentPage].content}</p>
                      <ShieldAlert className="text-red-700 w-12 h-12 mx-auto opacity-50" />
                    </div>
                  ) : (
                    <>
                      <div className="w-full bg-black/80 p-6 rounded border-l-8 border-red-600 text-left">
                        <span className="text-[10px] text-red-500 font-black uppercase mb-2 block">Descripción Visual del Panel:</span>
                        <p className="text-lg text-neutral-200 italic leading-snug">"{pages[currentPage].visual}"</p>
                      </div>
                      
                      <div className="w-full space-y-4">
                        {pages[currentPage].dialogue && pages[currentPage].dialogue.map((d, i) => (
                          <div key={i} className={`flex flex-col ${d.char === 'CAOOS' || d.char === 'JUNGKOOK' ? 'items-start' : 'items-end'}`}>
                            <span className="text-[10px] font-black text-red-600 mb-1 tracking-tighter">{d.char}</span>
                            <div className={`p-3 rounded-md text-sm font-bold max-w-[80%] ${
                              d.char === 'CAOOS' || d.char === 'JUNGKOOK' 
                              ? 'bg-neutral-100 text-black rounded-bl-none shadow-[4px_4px_0_rgba(220,38,38,1)]' 
                              : 'bg-neutral-800 text-neutral-300 rounded-br-none border border-neutral-700'
                            }`}>
                              {d.text}
                            </div>
                          </div>
                        ))}
                      </div>
                    </>
                  )}
                </div>

                {!pages[currentPage].isCover && !pages[currentPage].isEnd && (
                  <div className="mt-8 pt-4 border-t border-neutral-800 text-neutral-500 text-[10px] uppercase tracking-widest flex justify-between">
                    <span>{pages[currentPage].description}</span>
                    <Lock size={12} className="text-red-900" />
                  </div>
                )}
              </div>

            </div>

            {/* Controls */}
            <div className="mt-6 flex justify-between gap-4">
              <button 
                onClick={prevPage}
                disabled={currentPage === 0}
                className="flex-1 py-4 bg-neutral-800 hover:bg-neutral-700 disabled:opacity-20 rounded font-black uppercase text-xs flex items-center justify-center transition-all"
              >
                <ChevronLeft className="mr-2" /> Anterior
              </button>
              <button 
                onClick={nextPage}
                disabled={currentPage === pages.length - 1}
                className="flex-1 py-4 bg-red-700 hover:bg-red-600 disabled:opacity-20 rounded font-black uppercase text-xs flex items-center justify-center text-black shadow-lg transition-all active:scale-95"
              >
                Siguiente <ChevronRight className="ml-2" />
              </button>
            </div>
          </div>
        )}
      </main>

      <footer className="w-full p-8 text-center text-neutral-700 text-[10px] uppercase tracking-[0.4em] font-black">
        CAOOS SUPREMACY • CREADO POR @{contactInfo} • 2024
      </footer>
    </div>
  );
};

export default App;

```
