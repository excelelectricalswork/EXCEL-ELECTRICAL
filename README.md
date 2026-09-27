{
  "name": "Excel Electricals Choondy Aluva",
  "description": "Specialized electric motor rewinding workshop in Choondy, Aluva. Single-phase, 3-phase induction motors, submersible borewell pumps, industrial stators, Class H insulation, and motor overhauling.",
  "requestFramePermissions": [],
  "majorCapabilities": ["MAJOR_CAPABILITY_SERVER_SIDE_GEMINI_API"]
}

<!doctype html>
<html lang="en" class="scroll-smooth">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Excel Electricals Choondy Aluva – Electric Motor Rewinding & Pump Specialists</title>
    <meta name="description" content="Specialist electric motor winding workshop in Choondy, Aluva. 3-Phase induction motors, submersible borewell pumps, monobloc, Class H copper rewinding, and pump overhauling." />
    <meta property="og:title" content="Excel Electricals Choondy Aluva – Electric Motor Rewinding & Pump Specialists" />
    <meta property="og:description" content="Specialist electric motor winding workshop in Choondy, Aluva. 3-Phase induction motors, submersible borewell pumps, monobloc, Class H copper rewinding, and pump overhauling." />
    <meta property="og:type" content="website" />
    <meta property="og:site_name" content="Excel Electricals Motor Rewinding" />
    <meta name="twitter:card" content="summary_large_image" />
    <meta name="twitter:title" content="Excel Electricals Choondy Aluva – Electric Motor Rewinding & Pump Specialists" />
    <meta name="twitter:description" content="Specialist electric motor winding workshop in Choondy, Aluva. 3-Phase induction motors, submersible borewell pumps, monobloc, Class H copper rewinding, and pump overhauling." />
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=Syne:wght@600;700;800&display=swap" rel="stylesheet">
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Electrician",
      "name": "Excel Electricals",
      "image": "https://images.unsplash.com/photo-1621905251189-08b45d6a269e",
      "telephone": "+918590259451",
      "email": "excelelectricalswork@gmail.com",
      "address": {
        "@type": "PostalAddress",
        "streetAddress": "Near Choondy Junction, Aluva - Perumbavoor Road",
        "addressLocality": "Aluva",
        "addressRegion": "Kerala",
        "postalCode": "683112",
        "addressCountry": "IN"
      },
      "geo": {
        "@type": "GeoCoordinates",
        "latitude": 10.1076,
        "longitude": 76.3516
      },
      "url": "https://excelelectricals.in",
      "openingHoursSpecification": [
        {
          "@type": "OpeningHoursSpecification",
          "dayOfWeek": [
            "Monday",
            "Tuesday",
            "Wednesday",
            "Thursday",
            "Friday",
            "Saturday"
          ],
          "opens": "08:30",
          "closes": "20:00"
        },
        {
          "@type": "OpeningHoursSpecification",
          "dayOfWeek": "Sunday",
          "opens": "09:00",
          "closes": "14:00"
        }
      ],
      "priceRange": "₹₹",
      "areaServed": [
        "Choondy",
        "Aluva",
        "Edathala",
        "Companypady",
        "Kakkanad",
        "Perumbavoor",
        "Kochi",
        "Ernakulam"
      ]
    }
    </script>
  </head>
  <body class="bg-neutral-50 text-neutral-900 font-sans antialiased selection:bg-amber-400 selection:text-neutral-900">
    <div id="root"></div>
    <script type="module" src="/src/main.tsx"></script>
  </body>
</html>

@import "tailwindcss";

@layer base {
  :root {
    --font-sans: 'Plus Jakarta Sans', system-ui, -apple-system, sans-serif;
    --font-display: 'Syne', system-ui, -apple-system, sans-serif;
  }

  body {
    font-family: var(--font-sans);
    color: #171717;
  }

  .font-display {
    font-family: var(--font-display);
  }
}
export interface MotorServiceItem {
  id: string;
  number: string;
  title: string;
  tag: string;
  shortDesc: string;
  fullDesc: string;
  image: string;
  keySpecs: { label: string; value: string }[];
  processSteps: string[];
  insulationClass: string;
  warranty: string;
  turnaroundTime: string;
  applicableMotors: string[];
  materialsUsed: string[];
}

export interface MotorJobItem {
  id: string;
  title: string;
  category: 'submersible' | 'industrial' | 'monobloc';
  capacity: string;
  location: string;
  description: string;
  image: string;
  technicalSpecs: {
    hpRating: string;
    phase: string;
    polesRpm: string;
    slotCount: string;
    wireSwg: string;
    insulation: string;
    varnishBaking: string;
    meggerReading: string;
  };
  symptomsResolved: string[];
  client: string;
}

export interface WindingFaq {
  q: string;
  a: string;
}

export interface MotorEstimateOptions {
  motorType: 'submersible' | 'induction-3phase' | 'monobloc' | 'openwell';
  hp: number;
  rpm: '2880' | '1440' | '960';
  copperGrade: 'pure-class-f' | 'dual-coat-class-h';
  includeBearings: boolean;
  includeMechanicalSeal: boolean;
  expressTurnaround: boolean;
}

export interface WindingBookingData {
  name: string;
  phone: string;
  location: string;
  motorType: string;
  hpRating: string;
  problemDesc: string;
  pickupRequired: boolean;
}
import { MotorServiceItem, MotorJobItem, WindingFaq } from '../types';

export const MOTOR_WORKSHOP_INFO = {
  name: 'Excel Electricals',
  division: 'Motor Rewinding & Pump Engineering Division',
  tagline: 'Precision Copper Winding, Stator Overhaul & Pump Reconditioning',
  address: 'Near Choondy Junction, Aluva - Perumbavoor Road, Choondy, Aluva, Ernakulam, Kerala 683112',
  shortLocation: 'Choondy, Aluva, Kerala',
  landmark: 'Near Choondy Bypass Junction, Opposite Reliance Smart Point / Bus Stop',
  phonePrimary: '+91 85902 59451',
  phoneSecondary: '+91 85902 59451',
  phonePrimaryRaw: '918590259451',
  phoneSecondaryRaw: '918590259451',
  email: 'excelelectricalswork@gmail.com',
  licenseNo: 'KSEB / ELEC / EKM-2849',
  yearsExperience: 22,
  copperGuarantee: '100% Super Enameled EC Grade Virgin Copper Wire (Finolex / Precision)',
  emergencyBreakdown: 'Same-Day Fast Track Service for Industrial & Agricultural Pumps',
  regularHours: 'Mon – Sat: 8:00 AM – 8:30 PM | Sun: 9:00 AM – 2:00 PM (Emergency Drop-off Available)',
  pickupCoverage: [
    'Choondy',
    'Aluva Industrial Area',
    'Edathala',
    'Companypady',
    'Vazhakkulam',
    'Perumbavoor Timber Belt',
    'Kalamassery',
    'Eloor / FACT Belt',
    'Kakkanad',
    'Angamaly',
  ],
};

export const MOTOR_SERVICES_DATA: MotorServiceItem[] = [
  {
    id: 'submersible-borewell-rewinding',
    number: '01',
    title: 'Submersible Borewell & Openwell Pump Rewinding',
    tag: 'Borewell & Well Pumps',
    shortDesc: 'Water-lubricated submersible stators rewound with heavy-duty poly-wrapped high-dielectric waterproof copper winding wire.',
    fullDesc: 'Complete dismantling, stripping, and high-precision rewinding for 4-inch, 6-inch, and 8-inch submersible pump motors (single-phase and 3-phase). We use high-dielectric waterproof polypropylene/PVC insulated copper winding wire specifically engineered for continuous underwater submersion. The stator slots are lined with heavy Mylar/Nomex insulation, joints are sealed with waterproof vulcanized tape, and motors undergo hydraulic pressure and underwater insulation testing at 1000V.',
    image: '/src/assets/images/sub_pump_stator_1790491832919.jpg',
    keySpecs: [
      { label: 'Wire Specification', value: 'Poly-wrapped Waterproof Copper Submersible Wire' },
      { label: 'Insulation Class', value: 'Class B / Water Cooled (up to 90°C)' },
      { label: 'Testing Standard', value: '1,000V Underwater Megger (>200 MΩ)' },
      { label: 'Hardware Replaced', value: 'Carbon/SS Thrust Bearings, Bushings, Sand Guards' },
    ],
    processSteps: [
      'Stator core chemical descaling & sand removal',
      'Accurate coil dimension forming on precision winding jigs',
      'Slot insulation insertion with Nomex/Polyester composite sheets',
      'Hand-insertion and wooden/FRP slot wedge locking',
      'Waterproof resin cable jointing & 24-hr underwater immersion test',
    ],
    insulationClass: 'Class B / Waterproof Poly Coated',
    warranty: '6 Months Full Workshop Guarantee',
    turnaroundTime: '24 to 48 Hours',
    applicableMotors: ['Texmo', 'CRI', 'Kirloskar', 'Suguna', 'Crompton', 'Grundfos', 'Falcon', 'V-Guard'],
    materialsUsed: ['Poly-wrapped Copper Wire', 'Nomex Class F Paper', 'Carbon Thrust Bearings', 'Mechanical Seals'],
  },
  {
    id: 'three-phase-induction-rewinding',
    number: '02',
    title: '3-Phase Heavy Industrial Induction Motor Rewinding',
    tag: 'Industrial LT Motors',
    shortDesc: 'Stator rewinding for 1 HP to 125+ HP factory motors with Class H (180°C) dual-coated copper and vacuum varnish baking.',
    fullDesc: 'Heavy-duty stator coil winding for 3-phase squirrel cage and slip-ring induction motors operating in harsh industrial environments (crushers, plywood mills, rice mills, chemical units). Stripped without torch overheating to preserve lamination magnetic permeability. Wound using dual-coated modified polyester base with polyamide-imide topcoat (200°C thermal index), vacuum impregnated with Class H synthetic resin, and baked in temperature-controlled ovens.',
    image: '/src/assets/images/heavy_stator_75hp_1790491744750.jpg',
    keySpecs: [
      { label: 'Wire Grade', value: 'Dual-Coated Class H / Class 200 Enameled Copper' },
      { label: 'Insulation Class', value: 'Class H (180°C Operating Rating)' },
      { label: 'Slot Liners', value: 'Nomex-Kapton-Nomex (NKN) Composite Tri-laminate' },
      { label: 'Impregnation', value: 'Vacuum Resin Dip & 140°C Oven Baking for 6 Hours' },
    ],
    processSteps: [
      'Core-loss testing to ensure stator lamination integrity',
      'Micrometer wire gauge (SWG) check & turns per coil counter verification',
      'Diamond coil pre-forming and end-turn shaping for air circulation',
      'Inter-phase Nomex separation barriers between phase coils',
      'Surge comparison test (up to 3.5kV) & no-load current balance test',
    ],
    insulationClass: 'Class H (180°C) / Class 200',
    warranty: '12 Months Industrial Heavy-Duty Warranty',
    turnaroundTime: '2 to 4 Days (Fast-Track Available)',
    applicableMotors: ['Siemens', 'ABB', 'Bharat Bijlee (BBL)', 'Crompton Greaves', 'Kirloskar Electric', 'L&T', 'Havells'],
    materialsUsed: ['Precision / Finolex Dual-Coat Copper', 'Dr. Beck Synthetic Resin', 'NKN Nomex Paper', 'Fiberglass Sleeving'],
  },
  {
    id: 'monobloc-agricultural-rewinding',
    number: '03',
    title: 'Agricultural & Domestic Monobloc Pump Rewinding',
    tag: 'Surface & Monobloc',
    shortDesc: 'Centrifugal, self-priming, and high-head monobloc motors rewound with Class F copper, mechanical seal replacement, and impeller balancing.',
    fullDesc: 'Specialized reconditioning of residential and agricultural monobloc pumps experiencing coil burnout due to low voltage or dry run. We completely rewire the stator with premium copper winding, replace burnt run/start capacitors with genuine heavy-duty capacitors, replace worn ceramic-graphite mechanical water seals, and fit new SKF/NBC low-friction deep groove ball bearings.',
    image: '/src/assets/images/stator_bench_winding_1790491865309.jpg',
    keySpecs: [
      { label: 'Wire Specification', value: 'Super Enameled Copper Wire (Class F 155°C)' },
      { label: 'Capacitor Replacement', value: 'Heavy Duty 440V Metallized Polypropylene' },
      { label: 'Mechanical Seal', value: 'Silicon Carbide / Carbon Ceramic Seal Set' },
      { label: 'Bearings Fitted', value: 'SKF / NBC C3 High-Speed Shielded Bearings' },
    ],
    processSteps: [
      'Motor disassembly & hydraulic bearing puller extraction',
      'Inspection of rotor shaft run-out and bearing journals',
      'Stator rewinding with accurate original coil pitch & turns',
      'Mechanical seal seating on bronze/cast-iron pump volute',
      'Bench testing for suction pressure, discharge head, and silent running',
    ],
    insulationClass: 'Class F (155°C)',
    warranty: '6 Months Replacement Guarantee',
    turnaroundTime: 'Same Day / 24 Hours',
    applicableMotors: ['Texmo Taro', 'Kirloskar Jalraaj', 'CRI Master', 'Crompton Mini Champ', 'V-Guard Nova', 'Sharp'],
    materialsUsed: ['Class F Copper Wire', 'Epoxy Insulating Varnish', 'SKF Bearings', 'Ceramic Mechanical Seals'],
  },
];

export const MOTOR_JOBS_GALLERY: MotorJobItem[] = [
  {
    id: 'job-1',
    title: '25 HP 4-Pole 3-Phase Induction Stator Rewinding',
    category: 'industrial',
    capacity: '25 HP / 18.5 kW',
    location: 'Choondy Industrial Belt, Aluva',
    description: 'Heavy sawmill conveyor motor burnt due to single-phasing on phase B. Stator completely stripped, 48 slots lined with Nomex Class H paper, rewound with double-coated copper wire, and laced with high-grade white binding tape.',
    image: '/src/assets/images/stator_rewind_25hp_1790491723033.jpg',
    technicalSpecs: {
      hpRating: '25 HP (18.5 kW) 415V',
      phase: '3-Phase Delta Connected',
      polesRpm: '4 Poles / 1,460 RPM',
      slotCount: '48 Slots (Pitch 1-11)',
      wireSwg: '19.5 SWG + 20 SWG (Dual Parallel)',
      insulation: 'Nomex-Kapton Class H (180°C)',
      varnishBaking: 'Dr. Beck Synthetic Varnish, 140°C Cured',
      meggerReading: 'Inf. (>500 MΩ at 1,000V DC)',
    },
    symptomsResolved: [
      'Two phases completely charred due to contactor failure',
      'Rotor rubbed against stator causing local lamination burrs',
      'Smooth current draw achieved across all 3 phases (34A)',
    ],
    client: 'Aluva Plywood & Sawmill Co-op',
  },
  {
    id: 'job-2',
    title: '75 HP Heavy Industrial LT Stator Overhaul',
    category: 'industrial',
    capacity: '75 HP / 55 kW',
    location: 'Choondy Factory Zone, Aluva',
    description: 'Crusher motor stator rewinding. Cast iron ribbed housing with lifting lugs, large slot depth, high-temperature Nomex slot liners, dual-coat Class H copper wire with precise overhang forming.',
    image: '/src/assets/images/heavy_stator_75hp_1790491744750.jpg',
    technicalSpecs: {
      hpRating: '75 HP (55 kW) 415V',
      phase: '3-Phase Star-Delta Connected',
      polesRpm: '4 Poles / 1,480 RPM',
      slotCount: '72 Slots (Pitch 1-14)',
      wireSwg: '17 SWG Multi-strand Dual Coat',
      insulation: 'NKN Nomex-Kapton Class H (180°C)',
      varnishBaking: 'Double Vacuum Pressure Impregnation',
      meggerReading: '>1,000 MΩ at 1,000V DC Megger',
    },
    symptomsResolved: [
      'Inter-turn insulation breakdown caused by harsh voltage spikes',
      'Core cleaned and tested for minimal eddy-current loss',
      'Passed 3.5kV high-voltage surge withstand test',
    ],
    client: 'Granite & Aggregates Crushing Plant, Aluva',
  },
  {
    id: 'job-3',
    title: 'Vertical Inline Multistage Booster Pump Overhaul',
    category: 'submersible',
    capacity: '10 HP Multistage Unit',
    location: 'Aluva Commercial Complex',
    description: 'High-head vertical multistage pressure booster pump servicing a 12-floor commercial building. Stator rewound, shaft aligned, stainless steel barrel and ceramic-carbon mechanical seals overhauled.',
    image: '/src/assets/images/booster_pump_unit_1790491763260.jpg',
    technicalSpecs: {
      hpRating: '10 HP (7.5 kW) 415V',
      phase: '3-Phase 50Hz',
      polesRpm: '2 Poles / 2,900 RPM',
      slotCount: '24 Slots High-Speed',
      wireSwg: '18.5 SWG Class F',
      insulation: 'Dual Mylar & Nomex Phase Barriers',
      varnishBaking: 'Oven Cured at 135°C for 6 Hours',
      meggerReading: '350 MΩ after re-assembly',
    },
    symptomsResolved: [
      'Low water pressure across upper floors due to seal leakage',
      'Water ingress into lower bearing cavity arrested',
      'Full 14 bar head pressure restored',
    ],
    client: 'Commercial Complex Facility Management',
  },
  {
    id: 'job-4',
    title: 'Large Diameter Rotor / Stator Ring Coil Winding',
    category: 'industrial',
    capacity: 'Large Frame Specialty Motor',
    location: 'Aluva Industrial Corridor',
    description: 'Specialty large-diameter stator ring coil winding on our workshop jig with internal ventilation ducts, concentric copper coil groups tightly laced with white high-tensile Nomex binding tape.',
    image: '/src/assets/images/large_rotor_winding_1790491779757.jpg',
    technicalSpecs: {
      hpRating: 'Specialty High-Torque Frame',
      phase: '3-Phase Ring Distributed',
      polesRpm: '6 Poles / 960 RPM',
      slotCount: '54 Slots Ventilated',
      wireSwg: '18 SWG Heavy Enamel',
      insulation: 'Class H Nomex & Glass Cloth Ties',
      varnishBaking: 'Deep Dip & Oven Baked',
      meggerReading: '>500 MΩ at 1,000V DC',
    },
    symptomsResolved: [
      'Mechanical friction damage on outer winding turns repaired',
      'Air gap clearances matched to original factory blueprints',
      'Whisper-quiet high torque performance verified',
    ],
    client: 'Heavy Engineering Works, Aluva',
  },
  {
    id: 'job-5',
    title: 'Complete 3-Phase Induction Motor Assembly & Refurbishment',
    category: 'industrial',
    capacity: '15 HP / 11 kW Complete Unit',
    location: 'Choondy Workshop Bench, Aluva',
    description: 'Fully refurbished and repainted cast iron 3-phase induction motor with new terminal box, precision-ground keyed drive shaft, fitted with genuine SKF C3 deep groove bearings, and full-load tested.',
    image: '/src/assets/images/induction_motor_blue_1790491796327.jpg',
    technicalSpecs: {
      hpRating: '15 HP 415V 3-Phase',
      phase: '3-Phase Delta Connected',
      polesRpm: '4 Poles / 1,440 RPM',
      slotCount: '36 Slots',
      wireSwg: '19 SWG Dual Strand',
      insulation: 'Class H Nomex',
      varnishBaking: 'Double Vacuum Impregnation',
      meggerReading: 'Infinite (>1,000 MΩ)',
    },
    symptomsResolved: [
      'Bearing locked causing rotor scoring and thermal breakdown',
      'End bells re-sleeved to restore concentric bearing fits',
      'Full load test run completed with balanced amp draw (21A)',
    ],
    client: 'Timber Processing Unit, Perumbavoor Road',
  },
  {
    id: 'job-6',
    title: 'Borewell Submersible Pump Stator Coil Rewinding',
    category: 'submersible',
    capacity: '7.5 HP 100mm Borewell',
    location: 'Edathala, Aluva',
    description: 'Borewell submersible pump motor rewound with pure waterproof poly-coated copper winding wire, tight end-turn lacing, replaced carbon thrust shoes, and tested under 1,000V immersion.',
    image: '/src/assets/images/sub_pump_stator_1790491832919.jpg',
    technicalSpecs: {
      hpRating: '7.5 HP 415V 3-Phase',
      phase: '3-Phase Star Connected',
      polesRpm: '2 Poles / 2,880 RPM',
      slotCount: '24 Slots (Pitch 1-9)',
      wireSwg: '1.2mm Polypropylene Covered Copper',
      insulation: 'Multi-layer Poly/BOPP Water Seal',
      varnishBaking: 'Water-lubricated Stator Cavity',
      meggerReading: '280 MΩ after 24-hr immersion test',
    },
    symptomsResolved: [
      'RCCB tripping immediately when pump switched on',
      'Sand ingress into bearing chamber cleaned and sealed',
      'Restored full agricultural borewell flow',
    ],
    client: 'Residential Villa Community, Edathala',
  },
  {
    id: 'job-7',
    title: 'Stator Terminal Block Dressing & Red Varnish Oven Baking',
    category: 'industrial',
    capacity: '30 HP Industrial Stator',
    location: 'Choondy Workshop Oven Bay',
    description: 'Stator cavity and end-turns coated with high-dielectric red anti-tracking insulating varnish and baked in temperature-controlled oven. Brass terminal studs dressed with color-coded lead sleeves.',
    image: '/src/assets/images/motor_varnishing_1790491849111.jpg',
    technicalSpecs: {
      hpRating: '30 HP 415V 3-Phase',
      phase: '6-Terminal Dual Voltage Block',
      polesRpm: '4 Poles / 1,450 RPM',
      slotCount: '48 Slots',
      wireSwg: '18 SWG Class H',
      insulation: 'Nomex Tri-laminate',
      varnishBaking: '140°C Oven Baking for 8 Hours',
      meggerReading: 'Infinite (>1,000 MΩ)',
    },
    symptomsResolved: [
      'Moisture absorption in coils causing periodic ground faults',
      'Solidified varnish prevents coil vibration and chafing',
      'All 6 terminal studs torqued with brass nuts & washers',
    ],
    client: 'Plastic Recycling Plant, Aluva',
  },
  {
    id: 'job-8',
    title: 'Workbench Stator Rewinding & Precision Slot Wedge Locking',
    category: 'monobloc',
    capacity: '5 HP Openwell / Monobloc Stator',
    location: 'Choondy Workshop Bench',
    description: 'Stator placed on winding bench undergoing insertion of Class F copper coils, Nomex slot paper lining, wooden slot wedges locking each coil group, and high-tensile lacing cord binding.',
    image: '/src/assets/images/stator_bench_winding_1790491865309.jpg',
    technicalSpecs: {
      hpRating: '5.0 HP 230V/415V',
      phase: 'Dual Connection',
      polesRpm: '2 Poles / 2,850 RPM',
      slotCount: '36 Slots',
      wireSwg: '18.5 SWG Pure Copper',
      insulation: 'Mylar-Nomex Composite Sheets',
      varnishBaking: 'Dip & Oven Baked at 130°C',
      meggerReading: '>400 MΩ at 500V DC',
    },
    symptomsResolved: [
      'Low voltage coil burnout during peak summer heat',
      'Coil overhang properly contoured to prevent rotor contact',
      'Instant start with high starting torque',
    ],
    client: 'Irrigation Pump Set, Vazhakkulam',
  },
  {
    id: 'job-9',
    title: '40 HP Heavy Stator Core Rewind & Inter-Phase Nomex Barriers',
    category: 'industrial',
    capacity: '40 HP / 30 kW',
    location: 'Choondy Industrial Gate, Aluva',
    description: 'High-voltage industrial induction motor stator core rewind with deep slot insertion, multi-layer phase separation barriers using pure Nomex paper, and dual-coat Class H enameled copper.',
    image: '/src/assets/images/deep_stator_winding_1790491811847.jpg',
    technicalSpecs: {
      hpRating: '40 HP (30 kW) 415V',
      phase: '3-Phase Delta Connected',
      polesRpm: '4 Poles / 1,470 RPM',
      slotCount: '48 Slots (Pitch 1-12)',
      wireSwg: '18 SWG + 19 SWG Dual Strand',
      insulation: 'Nomex Class H (180°C)',
      varnishBaking: 'Double Vacuum Pressure Impregnation (140°C)',
      meggerReading: '>800 MΩ at 1,000V DC',
    },
    symptomsResolved: [
      'Phase-to-phase short circuit from overheated original insulation',
      'Stator core laminations descaled and re-varnished',
      'Balanced current across all 3 phases (54A on full load)',
    ],
    client: 'Aluva Packaging & Paper Mills',
  },
  {
    id: 'job-10',
    title: 'Precision Stator Slot Coil Insertion & Wedge Locking',
    category: 'monobloc',
    capacity: '3 HP Single & 3-Phase Stators',
    location: 'Choondy Workshop Bench, Aluva',
    description: 'Precision hand-insertion of bright virgin copper coils into laminated stator core slots with slot liners, slot wedges pressed into place, and tight end-turn binding cord.',
    image: '/src/assets/images/motor_stator_rewinding_1790490869404.jpg',
    technicalSpecs: {
      hpRating: '3.0 HP 230V / 415V',
      phase: 'Single / 3-Phase',
      polesRpm: '2 Poles / 2,880 RPM',
      slotCount: '24 Slots High-Torque',
      wireSwg: '19.5 SWG Super Enameled',
      insulation: 'Nomex-Mylar Composite',
      varnishBaking: 'Dr. Beck Synthetic Resin Dipped',
      meggerReading: '>300 MΩ at 500V DC',
    },
    symptomsResolved: [
      'Winding burned out due to capacitor failure & locked rotor',
      'Slot insulation completely replaced with high thermal endurance Nomex',
      'Runs cool and whisper-quiet under continuous duty',
    ],
    client: 'Commercial Laundry Facility, Aluva',
  },
  {
    id: 'job-11',
    title: '5 HP Deep Borewell Submersible Waterproof Poly Wire Rewind',
    category: 'submersible',
    capacity: '5 HP Submersible Borewell',
    location: 'Edathala, Aluva',
    description: 'Water-lubricated submersible pump stator rewound using genuine waterproof poly-coated copper winding wire with vulcanized waterproof lead cable joints and underwater pressure seals.',
    image: '/src/assets/images/submersible_pump_rewind_1790490891159.jpg',
    technicalSpecs: {
      hpRating: '5.0 HP 415V 3-Phase',
      phase: '3-Phase Star Connected',
      polesRpm: '2 Poles / 2,900 RPM',
      slotCount: '24 Slots Deep Core',
      wireSwg: '1.1mm Polypropylene Insulated Copper',
      insulation: 'Waterproof Poly/BOPP Dual Shield',
      varnishBaking: 'Water-Filled Stator Chamber Tested',
      meggerReading: '>250 MΩ after 24-hr Water Submersion',
    },
    symptomsResolved: [
      'Water entered stator causing immediate ground fault trip',
      'Sand incursion removed from thrust bearing housing',
      'Pressure sealed and water circulation channels cleaned',
    ],
    client: 'Apartment Complex Borewell, Edathala',
  },
  {
    id: 'job-12',
    title: 'Automated Coil Forming & Pitch Gauge Jig Setup',
    category: 'industrial',
    capacity: 'Multi-HP Coil Groups',
    location: 'Choondy Coil Preparation Bay, Aluva',
    description: 'Precision diamond and concentric coil group forming on adjustable stepped winding jigs. Exact wire length and turn count ensured for equal phase resistance across all coils.',
    image: '/src/assets/images/industrial_coil_winding_1790490911625.jpg',
    technicalSpecs: {
      hpRating: 'Custom Coils 1 HP to 100 HP',
      phase: 'Concentric & Diamond Groups',
      polesRpm: '2, 4, 6 & 8 Poles',
      slotCount: 'Customizable Jig Spans',
      wireSwg: '16 to 24 SWG Pure Copper',
      insulation: 'Dual Enamel Coating',
      varnishBaking: 'Class H Compatibility',
      meggerReading: '0.00% Turn-to-Turn Flaw Rate',
    },
    symptomsResolved: [
      'Eliminated phase resistance imbalance caused by unequal wire length',
      'Optimized end-turn clearance for maximum motor airflow',
      'Consistent electromagnetic flux distribution',
    ],
    client: 'Excel Electricals Precision Coil Bay',
  },
  {
    id: 'job-13',
    title: 'Workshop Electrical Test Bench - 1000V Megger & Surge Testing',
    category: 'industrial',
    capacity: 'Comprehensive Inspection Bay',
    location: 'Choondy Testing Bench, Aluva',
    description: 'Post-winding quality assurance station equipped with digital megger insulation testers, winding micro-ohmmeter for resistance balance, and variable 3-phase test panel for no-load run testing.',
    image: '/src/assets/images/motor_testing_bench_1790490929305.jpg',
    technicalSpecs: {
      hpRating: 'Testing up to 150 HP Motors',
      phase: 'Single & 3-Phase 415V',
      polesRpm: 'All Speeds Monitored',
      slotCount: 'Universal Stator Clamping',
      wireSwg: 'Micro-ohm Phase Comparison',
      insulation: '500V & 1000V DC Insulation Testing',
      varnishBaking: 'Post-Cure Thermal Scan',
      meggerReading: 'Inf. (>1000 MΩ Standard Pass)',
    },
    symptomsResolved: [
      'Zero defective motors leave the workshop',
      'Verified ampere draw balance on all phases prior to customer handover',
      'Bearing vibration and temperature baseline logged',
    ],
    client: 'Quality Control Bench, Choondy Aluva',
  },
];

export const ALL_WORKSHOP_PHOTOS = [
  {
    id: 'photo-1',
    src: '/src/assets/images/heavy_stator_75hp_1790491744750.jpg',
    title: '75 HP Heavy Industrial Stator Core',
    category: 'Industrial Stator',
    description: 'Class H 180°C dual-coat copper wire insertion with Nomex NKN slot liners.',
  },
  {
    id: 'photo-2',
    src: '/src/assets/images/stator_rewind_25hp_1790491723033.jpg',
    title: '25 HP 3-Phase Induction Stator Rewinding',
    category: 'Induction Motors',
    description: '48-slot stator rewound with double parallel copper wire and laced end-turns.',
  },
  {
    id: 'photo-3',
    src: '/src/assets/images/sub_pump_stator_1790491832919.jpg',
    title: 'Submersible Borewell Pump Stator Winding',
    category: 'Submersible Pumps',
    description: 'Waterproof blue poly-wrapped pure copper winding wire for deep borehole motors.',
  },
  {
    id: 'photo-4',
    src: '/src/assets/images/stator_bench_winding_1790491865309.jpg',
    title: 'Workbench Stator Rewinding & Wedge Locking',
    category: 'Workshop Bench',
    description: 'Technician inserting copper coil groups into stator slots and locking with wooden wedges.',
  },
  {
    id: 'photo-5',
    src: '/src/assets/images/deep_stator_winding_1790491811847.jpg',
    title: '40 HP Stator Core & Inter-Phase Barriers',
    category: 'Industrial Stator',
    description: 'Deep slot winding with white Nomex phase barriers to prevent inter-phase shorts.',
  },
  {
    id: 'photo-6',
    src: '/src/assets/images/motor_varnishing_1790491849111.jpg',
    title: 'Stator Red Insulating Varnish & Oven Baking',
    category: 'Varnish & Curing',
    description: 'High-dielectric anti-tracking varnish application and 140°C thermal curing.',
  },
  {
    id: 'photo-7',
    src: '/src/assets/images/booster_pump_unit_1790491763260.jpg',
    title: 'Multistage Pressure Booster Pump Unit',
    category: 'Commercial Pumps',
    description: 'High-head multistage booster pump with refurbished stator, shaft seals, and volute.',
  },
  {
    id: 'photo-8',
    src: '/src/assets/images/induction_motor_blue_1790491796327.jpg',
    title: 'Completed 3-Phase Motor Assembly',
    category: 'Finished Motors',
    description: 'Fully reassembled cast-iron induction motor with new SKF C3 bearings and terminal box.',
  },
  {
    id: 'photo-9',
    src: '/src/assets/images/large_rotor_winding_1790491779757.jpg',
    title: 'Large Diameter Stator Ring Coil Winding',
    category: 'Heavy Machinery',
    description: 'Specialty high-torque stator ring with ventilation ducts and high-tensile lacing cord.',
  },
  {
    id: 'photo-10',
    src: '/src/assets/images/motor_stator_rewinding_1790490869404.jpg',
    title: 'Close-Up Copper Coil Insertion into Slots',
    category: 'Precision Winding',
    description: 'Detailed view of bright super-enameled copper wire being hand-inserted into laminated core.',
  },
  {
    id: 'photo-11',
    src: '/src/assets/images/submersible_pump_rewind_1790490891159.jpg',
    title: 'Borewell Submersible Poly-Wrapped Winding',
    category: 'Submersible Pumps',
    description: 'Waterproof insulated copper winding wire installed for complete water submersion.',
  },
  {
    id: 'photo-12',
    src: '/src/assets/images/industrial_coil_winding_1790490911625.jpg',
    title: 'Precision Coil Forming on Winding Jig',
    category: 'Coil Preparation',
    description: 'Adjustable stepped jig forming diamond coils with calibrated turns and wire tension.',
  },
  {
    id: 'photo-13',
    src: '/src/assets/images/motor_testing_bench_1790490929305.jpg',
    title: 'Calibrated Megger & Electrical Testing Bench',
    category: 'Quality Testing',
    description: 'High-voltage insulation resistance Megger tester, multimeter, and phase current balancer.',
  },
];

export const WORKSHOP_STANDARDS = [
  {
    title: '100% EC Grade Virgin Copper',
    desc: 'We never compromise with CCA (copper-clad aluminum) or reclaimed wire. Only certified 99.99% electrolytic copper from Finolex & Precision.',
  },
  {
    title: 'Calibrated Megger & Surge Testing',
    desc: 'Every motor must pass 500V/1000V DC insulation resistance testing (>100 MΩ) and coil surge comparison before leaving our workshop.',
  },
  {
    title: 'Temperature-Controlled Baking Oven',
    desc: 'Oven curing at 130°C–140°C ensures synthetic varnish deeply cures into the center of coils, preventing vibration and moisture ingress.',
  },
  {
    title: 'Genuine SKF & NBC Bearings Only',
    desc: 'We stock genuine deep groove ball bearings and cylindrical roller bearings with C3 clearance for high thermal expansion tolerance.',
  },
  {
    title: 'Accurate Slot & Pitch Replication',
    desc: 'We precisely record slot counts, coil span pitch, wire SWG gauge, and turns per coil before stripping to preserve factory torque curves.',
  },
  {
    title: 'Pick-Up & Delivery in Aluva Belt',
    desc: 'Heavy industrial motors and deep borewell pumps collected and delivered across Choondy, Edathala, Kalamassery, and Perumbavoor.',
  },
];

export const WINDING_FAQS: WindingFaq[] = [
  {
    q: 'How do I know if my electric motor or pump stator is burnt?',
    a: 'Key signs include: a distinct pungent burnt varnish odor, the circuit breaker or RCCB tripping immediately upon power switch-on, the motor humming loudly without spinning, low water discharge pressure, or severe motor housing overheating within minutes.',
  },
  {
    q: 'Do you use pure copper or copper-clad aluminum wire?',
    a: 'Excel Electricals strictly uses 100% Super Enameled Pure Electrolytic Virgin Copper (EC grade, 99.99% purity) from certified manufacturers (Finolex / Precision). We provide open inspection of the winding reels in our Choondy workshop.',
  },
  {
    q: 'What is the turnaround time for a submersible or monobloc pump rewind?',
    a: 'Standard domestic pumps (0.5 HP to 2 HP) are completed within 24 hours. For critical agricultural irrigation or industrial breakdown emergencies, we offer a fast-track same-day rewinding service if dropped off by 10:00 AM.',
  },
  {
    q: 'What warranty is provided on motor rewinding?',
    a: 'We offer a 6-month workshop workmanship warranty on domestic & submersible pumps and a 12-month warranty on industrial Class H induction motor rewinding, covering insulation integrity and winding workmanship.',
  },
  {
    q: 'Can you arrange pickup of heavy motors from our site in Aluva?',
    a: 'Yes. For motors above 5 HP or commercial complexes, we offer on-site inspection, motor decoupling, transportation to our Choondy workshop, and post-rewind reinstallation and alignment.',
  },
];
import React, { useState } from 'react';
import { Phone, Menu, X, ArrowUpRight, Zap, Wrench } from 'lucide-react';
import { MOTOR_WORKSHOP_INFO } from '../data/electricalData';

interface NavbarProps {
  onOpenBooking: () => void;
}

export const Navbar: React.FC<NavbarProps> = ({ onOpenBooking }) => {
  const [mobileMenuOpen, setMobileMenuOpen] = useState(false);

  const navLinks = [
    { label: 'Winding Photos', href: '#photos' },
    { label: 'Services', href: '#services' },
    { label: 'Case Studies', href: '#gallery' },
    { label: 'Standards', href: '#workshop' },
    { label: 'Breakdown Help', href: '#emergency' },
    { label: 'Drop-off & Contact', href: '#contact' },
  ];

  return (
    <header className="sticky top-0 z-40 bg-white/95 backdrop-blur-md border-b border-neutral-200">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="flex items-center justify-between h-20">
          {/* Brand & Wordmark */}
          <div className="flex flex-col">
            <a 
              href="#" 
              className="text-2xl font-extrabold tracking-tight text-neutral-900 font-display transition-colors hover:text-amber-700"
            >
              Excel Electricals
            </a>
            <span className="text-[11px] font-semibold text-amber-700 tracking-wide">
              Motor Rewinding & Pump Specialists · Choondy, Aluva
            </span>
          </div>

          {/* Clean text navigation links */}
          <nav className="hidden lg:flex items-center gap-6">
            {navLinks.map((link) => (
              <a
                key={link.label}
                href={link.href}
                className="text-xs font-semibold text-neutral-700 hover:text-neutral-950 transition-colors py-1 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-0.5 after:bg-amber-500 hover:after:w-full after:transition-all"
              >
                {link.label}
              </a>
            ))}
          </nav>

          {/* Primary Actions */}
          <div className="hidden sm:flex items-center gap-3">
            <a
              href={`tel:${MOTOR_WORKSHOP_INFO.phonePrimary}`}
              className="inline-flex items-center gap-2 px-3 py-2 text-xs font-semibold text-neutral-800 bg-neutral-100 hover:bg-neutral-200 rounded-lg transition-colors whitespace-nowrap"
            >
              <Phone className="w-3.5 h-3.5 text-amber-600" />
              <span>{MOTOR_WORKSHOP_INFO.phonePrimary}</span>
            </a>

            <button
              onClick={onOpenBooking}
              className="inline-flex items-center gap-1.5 px-4 py-2 text-xs font-bold text-neutral-950 bg-amber-400 hover:bg-amber-300 rounded-lg transition-all shadow-sm hover:shadow whitespace-nowrap active:scale-[0.98]"
            >
              <Wrench className="w-3.5 h-3.5" />
              <span>Book Rewind / Drop-off</span>
            </button>
          </div>

          {/* Mobile hamburger button */}
          <div className="flex lg:hidden items-center gap-2">
            <a
              href={`tel:${MOTOR_WORKSHOP_INFO.phonePrimary}`}
              aria-label="Call Excel Electricals"
              className="p-2 text-neutral-800 bg-amber-400 rounded-lg"
            >
              <Phone className="w-4 h-4" />
            </a>
            <button
              onClick={() => setMobileMenuOpen(!mobileMenuOpen)}
              className="p-2 text-neutral-700 hover:text-neutral-950 focus:outline-none"
              aria-label="Toggle navigation menu"
            >
              {mobileMenuOpen ? <X className="w-6 h-6" /> : <Menu className="w-6 h-6" />}
            </button>
          </div>
        </div>
      </div>

      {/* Mobile menu dropdown */}
      {mobileMenuOpen && (
        <div className="lg:hidden border-b border-neutral-200 bg-white px-4 pt-3 pb-6 shadow-xl">
          <div className="flex flex-col gap-2">
            <div className="text-xs font-medium text-neutral-500 px-3 py-1 flex items-center gap-1.5 border-b border-neutral-100">
              <Zap className="w-3.5 h-3.5 text-amber-600" />
              <span>Choondy, Aluva · Stator Rewinding & Submersibles</span>
            </div>
            {navLinks.map((link) => (
              <a
                key={link.label}
                href={link.href}
                onClick={() => setMobileMenuOpen(false)}
                className="px-3 py-2 text-base font-semibold text-neutral-800 hover:text-amber-600 hover:bg-neutral-50 rounded-md transition-colors"
              >
                {link.label}
              </a>
            ))}
            <div className="pt-3 border-t border-neutral-200 flex flex-col gap-2">
              <button
                onClick={() => {
                  setMobileMenuOpen(false);
                  onOpenBooking();
                }}
                className="w-full text-center py-2.5 px-4 text-sm font-bold text-neutral-950 bg-amber-400 hover:bg-amber-300 rounded-lg shadow-sm"
              >
                Book Motor Rewind / Request Pickup
              </button>
              <a
                href={`tel:${MOTOR_WORKSHOP_INFO.phonePrimary}`}
                className="w-full text-center py-2.5 px-4 text-sm font-semibold text-neutral-800 bg-neutral-100 hover:bg-neutral-200 rounded-lg flex items-center justify-center gap-2"
              >
                <Phone className="w-4 h-4 text-amber-600" />
                <span>Call {MOTOR_WORKSHOP_INFO.phonePrimary}</span>
              </a>
            </div>
          </div>
        </div>
      )}
    </header>
  );
};
import React from 'react';
import { Wrench, Phone, Calculator, ArrowRight, Zap, ShieldCheck, CheckCircle2 } from 'lucide-react';
import { MOTOR_WORKSHOP_INFO } from '../data/electricalData';

interface HeroProps {
  onOpenBooking: () => void;
  onScrollToContact: () => void;
}

export const Hero: React.FC<HeroProps> = ({ onOpenBooking, onScrollToContact }) => {
  return (
    <section className="relative overflow-hidden bg-neutral-950 text-white">
      {/* Background Motor Rewinding Visual with Rich Scrim */}
      <div className="absolute inset-0 z-0">
        <img
          src="/src/assets/images/heavy_stator_75hp_1790491744750.jpg"
          alt="Heavy industrial 75 HP induction motor stator rewinding at Excel Electricals Choondy Aluva"
          className="w-full h-full object-cover object-center opacity-30 brightness-95 filter"
        />
        <div className="absolute inset-0 bg-gradient-to-t from-neutral-950 via-neutral-950/80 to-neutral-950/60" />
      </div>

      <div className="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 pt-16 pb-20 lg:pt-24 lg:pb-28">
        <div className="max-w-3xl">
          {/* Editorial Trust Meta Line */}
          <div className="flex flex-wrap items-center gap-2 text-xs font-semibold text-amber-400 tracking-wider uppercase mb-5">
            <span className="flex items-center gap-1.5 text-amber-300">
              <Zap className="w-4 h-4 fill-amber-400 text-amber-400" />
              Specialist Electric Motor Rewinding Workshop
            </span>
            <span aria-hidden="true" className="text-neutral-500">·</span>
            <span className="text-neutral-300">Choondy Junction, Aluva</span>
            <span aria-hidden="true" className="text-neutral-500">·</span>
            <span className="text-emerald-400 font-bold">100% Virgin Copper Guaranteed</span>
          </div>

          {/* Primary Headline */}
          <h1 className="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white tracking-tight leading-[1.12] mb-6 font-display [text-wrap:balance]">
            Precision electric motor rewinding & submersible pump overhaul.
          </h1>

          {/* Subtitle */}
          <p className="text-lg sm:text-xl text-neutral-300 leading-relaxed mb-8 max-w-2xl">
            From 0.5 HP domestic monoblocs and deep borewell submersible pumps to 150+ HP heavy industrial 3-phase induction motors. Rewound with dual-coated Class H copper wire, Nomex slot insulation, and 140°C oven-baked synthetic varnish.
          </p>

          {/* Action CTAs */}
          <div className="flex flex-wrap items-center gap-4 mb-12">
            <button
              onClick={onOpenBooking}
              className="px-6 py-3.5 text-sm font-bold text-neutral-950 bg-amber-400 hover:bg-amber-300 rounded-lg transition-all shadow-lg hover:shadow-amber-400/20 flex items-center gap-2 active:scale-[0.98]"
            >
              <Wrench className="w-4 h-4" />
              <span>Book Motor Drop-Off / Pickup</span>
            </button>

            <a
              href={`https://wa.me/${MOTOR_WORKSHOP_INFO.phonePrimaryRaw}?text=Hello%20Excel%20Electricals%20Choondy,%20I%20have%20a%20motor%20winding%20inquiry.`}
              target="_blank"
              rel="noopener noreferrer"
              className="px-6 py-3.5 text-sm font-bold text-white bg-emerald-600 hover:bg-emerald-500 rounded-lg transition-all shadow-md flex items-center gap-2"
            >
              <span>WhatsApp: 85902 59451</span>
            </a>

            <button
              onClick={onScrollToContact}
              className="px-5 py-3.5 text-sm font-medium text-neutral-300 hover:text-white transition-colors flex items-center gap-2 underline underline-offset-4 decoration-neutral-600 hover:decoration-amber-400"
            >
              <span>Workshop Address & Hours</span>
            </button>
          </div>

          {/* Quantitative Workshop Stats */}
          <div className="pt-8 border-t border-neutral-800/80 grid grid-cols-2 sm:grid-cols-4 gap-6">
            <div>
              <div className="text-3xl font-extrabold text-white font-display tabular-nums">
                22+ <span className="text-amber-400 text-xl font-normal">Years</span>
              </div>
              <div className="text-xs text-neutral-400 mt-1">Motor Winding Craft</div>
            </div>

            <div>
              <div className="text-3xl font-extrabold text-white font-display tabular-nums">
                18,000+
              </div>
              <div className="text-xs text-neutral-400 mt-1">Motors & Pumps Rewound</div>
            </div>

            <div>
              <div className="text-3xl font-extrabold text-white font-display tabular-nums">
                100%
              </div>
              <div className="text-xs text-neutral-400 mt-1">EC Grade Copper (Zero CCA)</div>
            </div>

            <div>
              <div className="text-3xl font-extrabold text-white font-display tabular-nums">
                &lt; 24 <span className="text-amber-400 text-xl font-normal">Hrs</span>
              </div>
              <div className="text-xs text-neutral-400 mt-1">Fast-Track Turnaround</div>
            </div>
          </div>

          {/* Quick Photo Preview Strip */}
          <div className="mt-10 pt-6 border-t border-neutral-800/60">
            <div className="flex items-center justify-between mb-3 text-xs">
              <span className="text-neutral-400 font-medium">Real Workshop Photos:</span>
              <a
                href="#photos"
                className="text-amber-400 hover:text-amber-300 font-semibold inline-flex items-center gap-1 transition-colors"
              >
                <span>View all 13 photos</span>
                <ArrowRight className="w-3.5 h-3.5" />
              </a>
            </div>
            <div className="grid grid-cols-2 sm:grid-cols-4 gap-3">
              {[
                {
                  src: '/src/assets/images/motor_stator_rewinding_1790490869404.jpg',
                  label: 'Stator Coil Insertion',
                },
                {
                  src: '/src/assets/images/sub_pump_stator_1790491832919.jpg',
                  label: 'Borewell Submersible',
                },
                {
                  src: '/src/assets/images/heavy_stator_75hp_1790491744750.jpg',
                  label: '75 HP 3-Phase Core',
                },
                {
                  src: '/src/assets/images/motor_testing_bench_1790490929305.jpg',
                  label: 'Megger Testing Bench',
                },
              ].map((item, idx) => (
                <a
                  key={idx}
                  href="#photos"
                  className="group relative rounded-lg overflow-hidden border border-neutral-800 hover:border-amber-400/80 transition-all aspect-[4/3] block bg-neutral-900"
                >
                  <img
                    src={item.src}
                    alt={item.label}
                    className="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
                  />
                  <div className="absolute inset-0 bg-gradient-to-t from-neutral-950/90 via-transparent to-transparent" />
                  <span className="absolute bottom-1.5 left-2 right-2 text-[10px] font-bold text-white group-hover:text-amber-300 transition-colors line-clamp-1">
                    {item.label}
                  </span>
                </a>
              ))}
            </div>
          </div>
        </div>
      </div>
    </section>
  );
};
import React from 'react';
import { ArrowUpRight, CheckCircle2, Shield, Clock, Layers, Zap } from 'lucide-react';
import { MOTOR_SERVICES_DATA } from '../data/electricalData';
import { MotorServiceItem } from '../types';

interface ServicesSectionProps {
  onSelectService: (service: MotorServiceItem) => void;
  onOpenBookingWithService: (serviceId: string) => void;
}

export const ServicesSection: React.FC<ServicesSectionProps> = ({
  onSelectService,
  onOpenBookingWithService,
}) => {
  return (
    <section id="services" className="py-20 lg:py-28 bg-white border-b border-neutral-200">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        {/* Section Header */}
        <div className="max-w-3xl mb-16">
          <div className="text-xs font-bold text-amber-700 tracking-wider uppercase mb-2">
            Specialized Workshop Capabilities
          </div>
          <h2 className="text-3xl sm:text-4xl font-extrabold text-neutral-900 tracking-tight font-display [text-wrap:balance]">
            Complete stator rewinding, coil design, and pump reconditioning services.
          </h2>
          <p className="mt-4 text-base sm:text-lg text-neutral-600 leading-relaxed">
            Every motor entering our Choondy workshop is diagnosed with digital surge comparison testers, stripped without destructive overheating, rewound with virgin electrolytic copper, and dynamically tested before dispatch.
          </p>
        </div>

        {/* 3-Column Services Grid with Rich Photography & Technical Details */}
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          {MOTOR_SERVICES_DATA.map((service) => (
            <div
              key={service.id}
              className="group flex flex-col justify-between bg-neutral-50 rounded-2xl border border-neutral-200/90 overflow-hidden hover:border-neutral-300 transition-all hover:shadow-sm"
            >
              {/* Photo Banner with Scrim */}
              <div className="relative aspect-[16/9] bg-neutral-900 overflow-hidden">
                <img
                  src={service.image}
                  alt={service.title}
                  className="w-full h-full object-cover object-center group-hover:scale-105 transition-transform duration-500 ease-out"
                />
                <div className="absolute inset-0 bg-gradient-to-t from-neutral-950/80 via-transparent to-transparent" />
                <div className="absolute bottom-3 left-4 right-4 flex items-center justify-between text-xs text-white">
                  <span className="font-bold text-amber-400 uppercase tracking-wider text-[11px]">
                    {service.tag}
                  </span>
                  <span className="text-neutral-300 font-medium">
                    {service.turnaroundTime}
                  </span>
                </div>
              </div>

              {/* Card Body */}
              <div className="p-6 sm:p-7 flex flex-col justify-between flex-1">
                <div>
                  <div className="flex items-center justify-between text-xs text-neutral-500 font-semibold mb-2">
                    <span className="text-amber-700 font-bold text-sm tracking-tight">
                      {service.number}.
                    </span>
                    <span className="text-neutral-600 font-medium">
                      Warranty: {service.warranty}
                    </span>
                  </div>

                  <h3 className="text-xl font-bold text-neutral-900 mb-2 font-display group-hover:text-amber-700 transition-colors">
                    {service.title}
                  </h3>

                  <p className="text-xs sm:text-sm text-neutral-600 leading-relaxed mb-5">
                    {service.shortDesc}
                  </p>

                  {/* Technical Specs List */}
                  <div className="grid grid-cols-1 sm:grid-cols-2 gap-2 mb-6 p-3.5 bg-white rounded-xl border border-neutral-200/70 text-xs">
                    {service.keySpecs.map((spec, i) => (
                      <div key={i} className="flex flex-col">
                        <span className="text-[10px] text-neutral-400 font-semibold uppercase tracking-wider">
                          {spec.label}
                        </span>
                        <span className="font-semibold text-neutral-800 text-[11px]">
                          {spec.value}
                        </span>
                      </div>
                    ))}
                  </div>

                  {/* Brands Serviced */}
                  <div className="mb-6">
                    <div className="text-[10px] font-bold text-neutral-500 uppercase tracking-wider mb-1.5">
                      Common Brands Rewound:
                    </div>
                    <div className="flex flex-wrap gap-1.5">
                      {service.applicableMotors.slice(0, 6).map((m, idx) => (
                        <span
                          key={idx}
                          className="px-2 py-0.5 text-[11px] font-medium text-neutral-700 bg-neutral-200/60 rounded"
                        >
                          {m}
                        </span>
                      ))}
                    </div>
                  </div>
                </div>

                {/* Card Action Zone */}
                <div className="pt-4 border-t border-neutral-200/80 flex items-center justify-between gap-3">
                  <button
                    onClick={() => onSelectService(service)}
                    className="text-xs font-bold text-neutral-900 hover:text-amber-700 inline-flex items-center gap-1 transition-colors"
                  >
                    <span>View Winding Process & Specs</span>
                    <ArrowUpRight className="w-3.5 h-3.5" />
                  </button>

                  <button
                    onClick={() => onOpenBookingWithService(service.id)}
                    className="px-3.5 py-1.5 text-xs font-bold text-neutral-950 bg-amber-400 hover:bg-amber-300 rounded-lg transition-colors shadow-sm"
                  >
                    Book Rewind
                  </button>
                </div>
              </div>
            </div>
          ))}
        </div>

        {/* Emergency Burnout Banner */}
        <div className="mt-14 p-6 sm:p-8 bg-neutral-900 rounded-2xl text-white flex flex-col md:flex-row items-start md:items-center justify-between gap-6 border border-neutral-800">
          <div className="space-y-1">
            <div className="text-xs font-bold text-amber-400 uppercase tracking-wider flex items-center gap-1.5">
              <Zap className="w-4 h-4 fill-amber-400" />
              Emergency Agricultural & Factory Breakdown Service
            </div>
            <div className="text-lg font-bold">
              Pump tripped or factory motor smoking? Fast-track 12-hour turnaround available.
            </div>
            <p className="text-xs text-neutral-400">
              Bring your motor directly to our Choondy workshop (near Choondy bypass) or call our technician for immediate on-site inspection and uncoupling.
            </p>
          </div>

          <button
            onClick={() => onOpenBookingWithService('three-phase-induction-rewinding')}
            className="px-5 py-2.5 text-xs font-bold text-neutral-950 bg-amber-400 hover:bg-amber-300 rounded-lg whitespace-nowrap transition-colors"
          >
            Request Emergency Rewind
          </button>
        </div>
      </div>
    </section>
  );
};
import React, { useState } from 'react';
import { ArrowUpRight, Zap, CheckCircle2, Sliders, Shield } from 'lucide-react';
import { MOTOR_JOBS_GALLERY, MOTOR_WORKSHOP_INFO } from '../data/electricalData';
import { MotorJobItem } from '../types';

interface ProjectsSectionProps {
  onSelectProject: (project: MotorJobItem) => void;
}

export const ProjectsSection: React.FC<ProjectsSectionProps> = ({ onSelectProject }) => {
  const [activeCategory, setActiveCategory] = useState<'all' | 'submersible' | 'industrial' | 'monobloc'>('all');

  const filteredJobs = activeCategory === 'all'
    ? MOTOR_JOBS_GALLERY
    : MOTOR_JOBS_GALLERY.filter((j) => j.category === activeCategory);

  return (
    <section id="gallery" className="py-20 lg:py-28 bg-white border-b border-neutral-200">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="flex flex-col md:flex-row md:items-end justify-between mb-12 gap-6">
          <div className="max-w-2xl">
            <div className="text-xs font-bold text-amber-700 tracking-wider uppercase mb-2">
              Workshop Gallery & Technical Case Studies
            </div>
            <h2 className="text-3xl sm:text-4xl font-extrabold text-neutral-900 tracking-tight font-display [text-wrap:balance]">
              Real motor winding jobs completed in our Choondy workshop.
            </h2>
            <p className="mt-3 text-sm text-neutral-600">
              Examining real slot pitches, wire SWG gauges, Nomex paper liners, and megger test results from actual repair jobs.
            </p>
          </div>

          {/* Interactive filter tabs */}
          <div className="flex flex-wrap items-center gap-1.5 p-1 bg-neutral-100 rounded-xl border border-neutral-200 self-start md:self-auto">
            {[
              { id: 'all', label: 'All Motors' },
              { id: 'industrial', label: '3-Phase Stators' },
              { id: 'submersible', label: 'Submersible Borewell' },
              { id: 'monobloc', label: 'Monobloc & Openwell' },
            ].map((tab) => (
              <button
                key={tab.id}
                type="button"
                onClick={() => setActiveCategory(tab.id as any)}
                className={`px-3.5 py-1.5 text-xs font-semibold rounded-lg transition-all whitespace-nowrap ${
                  activeCategory === tab.id
                    ? 'bg-white text-neutral-900 shadow-sm'
                    : 'text-neutral-600 hover:text-neutral-900'
                }`}
              >
                {tab.label}
              </button>
            ))}
          </div>
        </div>

        {/* Motor Jobs Grid */}
        <div className="grid grid-cols-1 md:grid-cols-2 gap-8">
          {filteredJobs.map((job) => (
            <div
              key={job.id}
              className="group flex flex-col bg-neutral-50 rounded-2xl border border-neutral-200 overflow-hidden hover:border-neutral-300 transition-all hover:shadow-sm"
            >
              {/* Photo Viewport */}
              <div className="relative aspect-[16/10] bg-neutral-900 overflow-hidden">
                <img
                  src={job.image}
                  alt={job.title}
                  className="w-full h-full object-cover object-center group-hover:scale-105 transition-transform duration-500 ease-out"
                />
                <div className="absolute inset-0 bg-gradient-to-t from-neutral-950/85 via-neutral-950/20 to-transparent" />

                {/* Overlaid Data */}
                <div className="absolute bottom-4 left-4 right-4 flex items-center justify-between text-xs text-white">
                  <span className="font-bold text-amber-400 font-display">
                    {job.capacity}
                  </span>
                  <span className="text-neutral-300">
                    {job.location}
                  </span>
                </div>
              </div>

              {/* Technical Job Information */}
              <div className="p-6 sm:p-7 flex flex-col justify-between flex-1">
                <div>
                  <h3 className="text-xl font-bold text-neutral-900 mb-2 font-display">
                    {job.title}
                  </h3>

                  <p className="text-xs sm:text-sm text-neutral-600 leading-relaxed mb-5">
                    {job.description}
                  </p>

                  {/* Deep Technical Parameters Table */}
                  <div className="grid grid-cols-2 gap-2 mb-5 p-3.5 bg-white rounded-xl border border-neutral-200/80 text-xs">
                    <div>
                      <span className="text-[10px] text-neutral-400 font-semibold uppercase block">
                        Slot Count & Pitch
                      </span>
                      <span className="font-semibold text-neutral-800 text-[11px]">
                        {job.technicalSpecs.slotCount}
                      </span>
                    </div>

                    <div>
                      <span className="text-[10px] text-neutral-400 font-semibold uppercase block">
                        Wire Gauge (SWG)
                      </span>
                      <span className="font-semibold text-neutral-800 text-[11px]">
                        {job.technicalSpecs.wireSwg}
                      </span>
                    </div>

                    <div>
                      <span className="text-[10px] text-neutral-400 font-semibold uppercase block">
                        Insulation Class
                      </span>
                      <span className="font-semibold text-neutral-800 text-[11px]">
                        {job.technicalSpecs.insulation}
                      </span>
                    </div>

                    <div>
                      <span className="text-[10px] text-neutral-400 font-semibold uppercase block">
                        Megger Insulation Test
                      </span>
                      <span className="font-bold text-emerald-700 text-[11px]">
                        {job.technicalSpecs.meggerReading}
                      </span>
                    </div>
                  </div>

                  {/* Symptoms Cured */}
                  <div className="space-y-1.5 mb-6">
                    <div className="text-[10px] font-bold text-neutral-500 uppercase tracking-wider">
                      Faults Diagnosed & Fixed:
                    </div>
                    {job.symptomsResolved.map((symp, i) => (
                      <div key={i} className="flex items-start gap-2 text-xs text-neutral-700">
                        <CheckCircle2 className="w-3.5 h-3.5 text-amber-600 shrink-0 mt-0.5" />
                        <span>{symp}</span>
                      </div>
                    ))}
                  </div>
                </div>

                {/* Footer Action */}
                <div className="pt-4 border-t border-neutral-200/80 flex items-center justify-between">
                  <button
                    onClick={() => onSelectProject(job)}
                    className="text-xs font-bold text-neutral-900 hover:text-amber-700 inline-flex items-center gap-1 transition-colors"
                  >
                    <span>Full Technical Case Study</span>
                    <ArrowUpRight className="w-3.5 h-3.5" />
                  </button>

                  <a
                    href={`https://wa.me/${MOTOR_WORKSHOP_INFO.phonePrimaryRaw}?text=Hello%20Excel%20Electricals,%20I%20have%20a%20motor%20similar%20to:%20${encodeURIComponent(job.title)}`}
                    target="_blank"
                    rel="noopener noreferrer"
                    className="text-xs font-semibold text-neutral-600 hover:text-neutral-900 transition-colors"
                  >
                    Inquire Similar Rewind
                  </a>
                </div>
              </div>
            </div>
          ))}
        </div>
      </div>
    </section>
  );
};
import React from 'react';
import { Phone, AlertTriangle, Clock, Wrench, CheckCircle2, ShieldAlert } from 'lucide-react';
import { MOTOR_WORKSHOP_INFO } from '../data/electricalData';

export const EmergencySection: React.FC = () => {
  return (
    <section id="emergency" className="py-20 lg:py-28 bg-neutral-950 text-white relative overflow-hidden border-b border-neutral-900">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
          {/* Left Column */}
          <div className="lg:col-span-6 space-y-6">
            <div className="flex items-center gap-2 text-xs font-bold text-amber-400 uppercase tracking-wider">
              <AlertTriangle className="w-4 h-4 text-amber-400" />
              <span>Urgent Motor Burnout & Breakdown Desk · Choondy Aluva</span>
            </div>

            <h2 className="text-3xl sm:text-4xl lg:text-5xl font-extrabold tracking-tight font-display text-white [text-wrap:balance]">
              Submersible pump failed or factory motor smoking? Call our workshop desk immediately.
            </h2>

            <p className="text-base text-neutral-300 leading-relaxed">
              If an electric motor hums without turning, trips the RCCB repeatedly, or gives off a pungent burnt-varnish smell, powering it on repeatedly can melt the laminated core. Switch off immediately and contact our Choondy workshop.
            </p>

            {/* Direct Calling Hotlines */}
            <div className="grid grid-cols-1 sm:grid-cols-2 gap-4 pt-2">
              <a
                href={`tel:${MOTOR_WORKSHOP_INFO.phonePrimary}`}
                className="p-5 bg-amber-400 hover:bg-amber-300 text-neutral-950 rounded-xl transition-all shadow-lg flex flex-col justify-between group active:scale-[0.98]"
              >
                <div>
                  <div className="text-[11px] font-bold uppercase tracking-wider text-neutral-800">
                    Direct Workshop Helpline
                  </div>
                  <div className="text-2xl font-extrabold font-display tabular-nums mt-1">
                    {MOTOR_WORKSHOP_INFO.phonePrimary}
                  </div>
                </div>
                <div className="mt-4 flex items-center gap-2 text-xs font-bold">
                  <Phone className="w-4 h-4 fill-neutral-950" />
                  <span>Click to Call 85902 59451</span>
                </div>
              </a>

              <a
                href={`https://wa.me/${MOTOR_WORKSHOP_INFO.phonePrimaryRaw}?text=URGENT%20MOTOR%20BREAKDOWN:%20My%20motor%20has%20tripped/burnt.`}
                target="_blank"
                rel="noopener noreferrer"
                className="p-5 bg-neutral-900 hover:bg-neutral-800 text-white border border-neutral-800 hover:border-neutral-700 rounded-xl transition-all flex flex-col justify-between active:scale-[0.98]"
              >
                <div>
                  <div className="text-[11px] font-bold uppercase tracking-wider text-emerald-400">
                    WhatsApp Photo Diagnostic
                  </div>
                  <div className="text-base font-bold text-white mt-1">
                    Send Motor Nameplate Photo
                  </div>
                </div>
                <div className="mt-4 flex items-center gap-2 text-xs font-bold text-amber-400">
                  <span>Open WhatsApp Diagnostic</span>
                </div>
              </a>
            </div>

            {/* Coverage Areas */}
            <div className="pt-4 border-t border-neutral-800/80 text-xs text-neutral-400">
              <div className="font-semibold text-neutral-300 mb-2">
                Motor Pickup & Uncoupling Coverage:
              </div>
              <div className="flex flex-wrap gap-2">
                {MOTOR_WORKSHOP_INFO.pickupCoverage.map((area, idx) => (
                  <span key={idx} className="text-neutral-400 after:content-['·'] after:ml-2 last:after:content-none">
                    {area}
                  </span>
                ))}
              </div>
            </div>
          </div>

          {/* Right Column: Pre-dropoff Checklist */}
          <div className="lg:col-span-6 bg-neutral-900/90 rounded-2xl border border-neutral-800 p-6 sm:p-8 space-y-6">
            <div className="flex items-center gap-3">
              <div className="p-2.5 rounded-lg bg-amber-500/10 text-amber-400">
                <ShieldAlert className="w-6 h-6" />
              </div>
              <div>
                <h3 className="text-lg font-bold text-white font-display">
                  What to Check Before Dropping Off Your Motor
                </h3>
                <p className="text-xs text-neutral-400">
                  Quick tests to confirm whether the problem is in the motor or the starter panel.
                </p>
              </div>
            </div>

            {/* Diagnostic Photo Banner */}
            <div className="relative rounded-xl overflow-hidden aspect-[21/9] border border-neutral-800">
              <img
                src="/src/assets/images/deep_stator_winding_1790491811847.jpg"
                alt="Motor stator winding inspection at Excel Electricals Choondy"
                className="w-full h-full object-cover"
              />
              <div className="absolute inset-0 bg-gradient-to-t from-neutral-950 via-neutral-950/40 to-transparent" />
              <div className="absolute bottom-2.5 left-3 right-3 flex items-center justify-between text-[11px] text-white">
                <span className="font-bold text-amber-400">Choondy Diagnostic Bay</span>
                <span className="text-neutral-300">Fast Megger & Surge Testing</span>
              </div>
            </div>

            <div className="space-y-3 text-xs text-neutral-300">
              <div className="flex items-start gap-2.5 p-3 rounded-lg bg-neutral-950/60 border border-neutral-800">
                <span className="w-5 h-5 rounded-full bg-amber-400/20 text-amber-400 flex items-center justify-center font-bold shrink-0 mt-0.5">
                  1
                </span>
                <span>
                  <strong>Check Starter Capacitor (Single-Phase):</strong> Often a motor that only hums without turning has a failed 36/50/72 µF starting or running capacitor, rather than a burnt winding. We test capacitors on arrival.
                </span>
              </div>

              <div className="flex items-start gap-2.5 p-3 rounded-lg bg-neutral-950/60 border border-neutral-800">
                <span className="w-5 h-5 rounded-full bg-amber-400/20 text-amber-400 flex items-center justify-center font-bold shrink-0 mt-0.5">
                  2
                </span>
                <span>
                  <strong>Rotate Shaft by Hand:</strong> If the shaft is physically jammed or gritty, the bearings or mechanical seal may have seized. Forcing power can burn an otherwise intact winding.
                </span>
              </div>

              <div className="flex items-start gap-2.5 p-3 rounded-lg bg-neutral-950/60 border border-neutral-800">
                <span className="w-5 h-5 rounded-full bg-amber-400/20 text-amber-400 flex items-center justify-center font-bold shrink-0 mt-0.5">
                  3
                </span>
                <span>
                  <strong>Bring the Terminal Box & Cover:</strong> Always bring the terminal block, fan cover, and pump volute so we can pressure test the complete re-assembled unit.
                </span>
              </div>
            </div>

            <div className="pt-4 border-t border-neutral-800 text-xs text-neutral-400">
              <div className="flex items-center gap-2">
                <Clock className="w-4 h-4 text-amber-400 shrink-0" />
                <span>
                  Drop off your motor at Choondy Junction by <strong>10:00 AM</strong> for same-day fast-track rewinding.
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  );
};
import React from 'react';
import { WORKSHOP_STANDARDS } from '../data/electricalData';
import { ShieldCheck, CheckCircle2, Zap } from 'lucide-react';

export const BrandsSection: React.FC = () => {
  return (
    <section id="workshop" className="py-20 lg:py-24 bg-neutral-50 border-b border-neutral-200">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="text-center max-w-3xl mx-auto mb-14">
          <div className="text-xs font-bold text-amber-700 uppercase tracking-wider mb-2">
            Quality Assurance & Material Engineering
          </div>
          <h2 className="text-3xl font-bold text-neutral-900 font-display [text-wrap:balance]">
            Why motors rewound at Excel Electricals last longer and run cooler
          </h2>
          <p className="mt-3 text-sm text-neutral-600">
            We reject cheap shortcuts. Every coil is wound with certified electrolytic virgin copper, insulated with Nomex Class H liners, and baked to full cure.
          </p>
        </div>

        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          {WORKSHOP_STANDARDS.map((std, idx) => (
            <div
              key={idx}
              className="p-6 bg-white rounded-xl border border-neutral-200/90 flex flex-col justify-between hover:border-neutral-300 transition-all hover:shadow-sm"
            >
              <div>
                <div className="flex items-center gap-2 mb-3">
                  <span className="w-6 h-6 rounded-full bg-amber-100 text-amber-800 text-xs font-bold flex items-center justify-center">
                    0{idx + 1}
                  </span>
                  <h3 className="text-base font-bold text-neutral-900 font-display">
                    {std.title}
                  </h3>
                </div>
                <p className="text-xs text-neutral-600 leading-relaxed">
                  {std.desc}
                </p>
              </div>

              <div className="mt-4 pt-3 border-t border-neutral-100 flex items-center gap-1.5 text-[11px] font-semibold text-emerald-700">
                <CheckCircle2 className="w-3.5 h-3.5 text-emerald-600" />
                <span>Verified Workshop Protocol</span>
              </div>
            </div>
          ))}
        </div>

        {/* Real Workshop Equipment & Process Photos */}
        <div className="mt-14">
          <div className="text-xs font-bold text-neutral-500 uppercase tracking-wider mb-4 text-center">
            Inside Our Choondy Motor Workshop
          </div>
          <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
            <div className="relative rounded-2xl overflow-hidden bg-neutral-900 border border-neutral-200 aspect-[16/10] group">
              <img
                src="/src/assets/images/industrial_coil_winding_1790490911625.jpg"
                alt="Precision coil winding jig in Choondy workshop"
                className="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
              />
              <div className="absolute inset-0 bg-gradient-to-t from-neutral-950/85 via-transparent to-transparent" />
              <div className="absolute bottom-3 left-4 right-4 text-white">
                <div className="text-[11px] font-bold text-amber-400 uppercase tracking-wider">Step 1: Coil Preparation</div>
                <div className="text-sm font-bold mt-0.5">Precision Stepped Coil Forming Jig</div>
                <div className="text-xs text-neutral-300 mt-0.5">Equal turn length eliminates phase resistance imbalance.</div>
              </div>
            </div>

            <div className="relative rounded-2xl overflow-hidden bg-neutral-900 border border-neutral-200 aspect-[16/10] group">
              <img
                src="/src/assets/images/motor_varnishing_1790491849111.jpg"
                alt="Motor stator red varnish baking oven at Excel Electricals"
                className="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
              />
              <div className="absolute inset-0 bg-gradient-to-t from-neutral-950/85 via-transparent to-transparent" />
              <div className="absolute bottom-3 left-4 right-4 text-white">
                <div className="text-[11px] font-bold text-amber-400 uppercase tracking-wider">Step 2: Insulating Varnish</div>
                <div className="text-sm font-bold mt-0.5">140°C Oven Baking Chamber</div>
                <div className="text-xs text-neutral-300 mt-0.5">Deep varnish penetration stops vibration and moisture ingress.</div>
              </div>
            </div>

            <div className="relative rounded-2xl overflow-hidden bg-neutral-900 border border-neutral-200 aspect-[16/10] group">
              <img
                src="/src/assets/images/motor_testing_bench_1790490929305.jpg"
                alt="1000V Megger and electrical test bench at Excel Electricals"
                className="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
              />
              <div className="absolute inset-0 bg-gradient-to-t from-neutral-950/85 via-transparent to-transparent" />
              <div className="absolute bottom-3 left-4 right-4 text-white">
                <div className="text-[11px] font-bold text-amber-400 uppercase tracking-wider">Step 3: Quality Testing</div>
                <div className="text-sm font-bold mt-0.5">1,000V Calibrated Megger Bench</div>
                <div className="text-xs text-neutral-300 mt-0.5">Insulation resistance verified &gt; 1,000 MΩ before dispatch.</div>
              </div>
            </div>
          </div>
        </div>

        {/* Copper Purity Guarantee Banner */}
        <div className="mt-12 p-5 bg-amber-50 rounded-xl border border-amber-200/80 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-amber-950">
          <div className="flex items-center gap-3">
            <div className="p-2 rounded-lg bg-amber-400 text-neutral-950 font-bold shrink-0">
              <Zap className="w-5 h-5 fill-neutral-950" />
            </div>
            <div>
              <div className="font-bold text-sm">Open Workshop Wire Verification Policy</div>
              <div className="text-amber-900 mt-0.5">
                Visit our Choondy workshop and inspect the copper wire spools, wire micrometer gauges, and insulation sleeves before we insert them into your stator.
              </div>
            </div>
          </div>
          <div className="text-right shrink-0">
            <span className="font-bold text-neutral-900 block font-display">Finolex & Precision Copper</span>
            <span className="text-[11px] text-amber-800">100% Super Enameled</span>
          </div>
        </div>
      </div>
    </section>
  );
};
import React from 'react';
import { Quote, Wrench, ShieldCheck, HelpCircle } from 'lucide-react';
import { WINDING_FAQS, MOTOR_WORKSHOP_INFO } from '../data/electricalData';

export const TestimonialsSection: React.FC = () => {
  const motorReviews = [
    {
      id: 'rev-1',
      name: 'M. K. Basheer',
      role: 'Production Supervisor, Aluva Wood Products',
      location: 'Choondy Industrial Gate',
      content: 'Our 25 HP bandsaw motor burnt out on a busy Tuesday morning. Excel Electricals rewound the 48-slot stator with Class H copper wire, baked it overnight in their oven, and delivered it by Wednesday noon. Smooth running and cool temperature even during 10-hour non-stop shifts.',
      motorType: '25 HP Sawmill Stator Rewind',
    },
    {
      id: 'rev-2',
      name: 'Varghese Mathew',
      role: 'Apartment Committee Secretary',
      location: 'Edathala, Aluva',
      content: 'Our 7.5 HP borewell pump was tripping the RCCB due to water leakage into the motor. Excel Electricals stripped the stator, used waterproof poly-wrapped copper wire, replaced the carbon thrust bearings, and tested it underwater. Running without issues for over 8 months now.',
      motorType: '7.5 HP Borewell Submersible',
    },
    {
      id: 'rev-3',
      name: 'C. P. Shaji',
      role: 'Dairy & Cardamom Farmer',
      location: 'Vazhakkulam / Aluva',
      content: 'I brought in my 3 HP Texmo openwell pump that hummed but would not start due to low voltage burnout. They replaced the start windings with genuine copper, changed the mechanical seal, and fitted new SKF bearings. Very reasonable charges and honest work.',
      motorType: '3 HP Openwell Agriculture Pump',
    },
  ];

  return (
    <section id="faqs" className="py-20 lg:py-28 bg-white border-b border-neutral-200">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        {/* Customer Reviews */}
        <div className="max-w-3xl mb-14">
          <div className="text-xs font-bold text-amber-700 tracking-wider uppercase mb-2">
            Local Customer Trust
          </div>
          <h2 className="text-3xl sm:text-4xl font-extrabold text-neutral-900 tracking-tight font-display [text-wrap:balance]">
            Trusted by factory operators, apartment complexes, and farmers across Aluva.
          </h2>
        </div>

        <div className="grid grid-cols-1 md:grid-cols-3 gap-8 mb-20">
          {motorReviews.map((r) => (
            <div
              key={r.id}
              className="bg-neutral-50 rounded-2xl border border-neutral-200/90 p-7 flex flex-col justify-between hover:border-neutral-300 transition-colors"
            >
              <div>
                <Quote className="w-7 h-7 text-amber-500/40 mb-4" />
                <p className="text-sm text-neutral-700 leading-relaxed mb-6">
                  "{r.content}"
                </p>
              </div>

              <div className="pt-4 border-t border-neutral-200/80">
                <div className="font-bold text-sm text-neutral-900 font-display">
                  {r.name}
                </div>
                <div className="text-xs text-neutral-600 mt-0.5">
                  {r.role}
                </div>
                <div className="text-xs text-neutral-500 mt-1 flex items-center gap-1.5">
                  <span>{r.location}</span>
                  <span aria-hidden="true">·</span>
                  <span className="text-amber-700 font-semibold">{r.motorType}</span>
                </div>
              </div>
            </div>
          ))}
        </div>

        {/* Winding FAQs Accordion Style */}
        <div className="bg-neutral-50 rounded-2xl border border-neutral-200 p-8 sm:p-10">
          <div className="max-w-2xl mb-8">
            <div className="flex items-center gap-2 text-xs font-bold text-amber-700 uppercase tracking-wider mb-1">
              <HelpCircle className="w-4 h-4 text-amber-600" />
              <span>Frequently Asked Questions</span>
            </div>
            <h3 className="text-2xl font-bold text-neutral-900 font-display">
              Motor Rewinding & Technical Guidelines
            </h3>
          </div>

          <div className="grid grid-cols-1 md:grid-cols-2 gap-6 text-xs">
            {WINDING_FAQS.map((faq, idx) => (
              <div key={idx} className="p-4 bg-white rounded-xl border border-neutral-200/80 space-y-2">
                <h4 className="font-bold text-neutral-900 text-sm">
                  {faq.q}
                </h4>
                <p className="text-neutral-600 leading-relaxed text-xs">
                  {faq.a}
                </p>
              </div>
            ))}
          </div>
        </div>
      </div>
    </section>
  );
};
import React, { useState } from 'react';
import { Phone, Mail, MapPin, Clock, Send, CheckCircle2, MessageSquare, ExternalLink, Wrench } from 'lucide-react';
import { MOTOR_WORKSHOP_INFO, MOTOR_SERVICES_DATA } from '../data/electricalData';
import { WindingBookingData } from '../types';

interface ContactSectionProps {
  prefilledService?: string;
  prefilledNote?: string;
}

export const ContactSection: React.FC<ContactSectionProps> = ({
  prefilledService,
  prefilledNote,
}) => {
  const [formData, setFormData] = useState<WindingBookingData>({
    name: '',
    phone: '',
    location: 'Choondy / Aluva',
    motorType: 'Submersible Borewell Pump',
    hpRating: '3.0 HP',
    problemDesc: prefilledNote || '',
    pickupRequired: false,
  });

  const [errors, setErrors] = useState<Record<string, string>>({});
  const [submitted, setSubmitted] = useState(false);
  const [ticketId, setTicketId] = useState('');

  const validate = () => {
    const newErrors: Record<string, string> = {};

    if (!formData.name.trim()) {
      newErrors.name = 'Please provide your full name.';
    }

    const cleanPhone = formData.phone.replace(/[\s-+()]/g, '');
    if (!cleanPhone || cleanPhone.length < 10) {
      newErrors.phone = 'Please enter a valid 10-digit contact number.';
    }

    if (!formData.location.trim()) {
      newErrors.location = 'Please state your locality in Aluva or surrounding areas.';
    }

    setErrors(newErrors);
    return Object.keys(newErrors).length === 0;
  };

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    if (!validate()) return;

    const generatedTicket = `MOT-${Math.floor(100000 + Math.random() * 900000)}`;
    setTicketId(generatedTicket);
    setSubmitted(true);
  };

  const handleWhatsAppSync = () => {
    const text = `*New Motor Rewinding Booking [${ticketId}]*%0A` +
      `• *Customer:* ${encodeURIComponent(formData.name)}%0A` +
      `• *Phone:* ${encodeURIComponent(formData.phone)}%0A` +
      `• *Location:* ${encodeURIComponent(formData.location)}%0A` +
      `• *Motor Type:* ${encodeURIComponent(formData.motorType)}%0A` +
      `• *HP Rating:* ${encodeURIComponent(formData.hpRating)}%0A` +
      `• *Pickup Needed:* ${formData.pickupRequired ? 'Yes (Aluva area)' : 'No (Direct Choondy drop-off)'}%0A` +
      `• *Symptoms:* ${encodeURIComponent(formData.problemDesc || 'Stator inspection requested')}`;

    window.open(`https://wa.me/${MOTOR_WORKSHOP_INFO.phonePrimaryRaw}?text=${text}`, '_blank');
  };

  return (
    <section id="contact" className="py-20 lg:py-28 bg-neutral-100/70 border-b border-neutral-200">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-12 items-start">
          {/* Left Column: Workshop Location & Contact Channels */}
          <div className="lg:col-span-5 space-y-8">
            <div>
              <div className="text-xs font-bold text-amber-700 tracking-wider uppercase mb-2">
                Workshop Desk & Drop-Off Point
              </div>
              <h2 className="text-3xl sm:text-4xl font-extrabold text-neutral-900 tracking-tight font-display [text-wrap:balance]">
                Drop off your motor at Choondy Junction or book pickup.
              </h2>
              <p className="mt-3 text-sm text-neutral-600 leading-relaxed">
                Conveniently located on the Aluva – Perumbavoor Road near Choondy Bypass. Ample space for vehicle unloading of heavy pumps and motors.
              </p>
            </div>

            <div className="space-y-4 text-sm">
              {/* Address */}
              <div className="p-4 bg-white rounded-xl border border-neutral-200/90 shadow-sm">
                <div className="flex items-start gap-3">
                  <MapPin className="w-5 h-5 text-amber-600 shrink-0 mt-0.5" />
                  <div>
                    <div className="font-bold text-neutral-900">Choondy Workshop & Testing Yard</div>
                    <div className="text-xs text-neutral-600 mt-1 leading-relaxed">
                      {MOTOR_WORKSHOP_INFO.address}
                    </div>
                    <div className="text-[11px] text-amber-800 font-semibold mt-1">
                      Landmark: {MOTOR_WORKSHOP_INFO.landmark}
                    </div>
                    <a
                      href="https://maps.google.com/?q=Choondy+Junction+Aluva+Kerala"
                      target="_blank"
                      rel="noopener noreferrer"
                      className="inline-flex items-center gap-1 text-xs font-bold text-neutral-900 hover:text-amber-700 mt-2 transition-colors"
                    >
                      <span>Open in Google Maps</span>
                      <ExternalLink className="w-3 h-3" />
                    </a>
                  </div>
                </div>
              </div>

              {/* Phone Contacts */}
              <div className="p-4 bg-white rounded-xl border border-neutral-200/90 shadow-sm">
                <div className="flex items-start gap-3">
                  <Phone className="w-5 h-5 text-amber-600 shrink-0 mt-0.5" />
                  <div>
                    <div className="font-bold text-neutral-900">Direct Workshop Phone & WhatsApp</div>
                    <div className="text-sm font-bold text-neutral-900 mt-1">
                      <a href={`tel:${MOTOR_WORKSHOP_INFO.phonePrimary}`} className="hover:text-amber-700 font-display">
                        {MOTOR_WORKSHOP_INFO.phonePrimary}
                      </a>
                    </div>
                    <div className="text-[11px] text-emerald-700 font-medium mt-0.5">
                      WhatsApp active on same number: <strong>{MOTOR_WORKSHOP_INFO.phonePrimaryRaw}</strong>
                    </div>
                  </div>
                </div>
              </div>

              {/* Email */}
              <div className="p-4 bg-white rounded-xl border border-neutral-200/90 shadow-sm">
                <div className="flex items-start gap-3">
                  <Mail className="w-5 h-5 text-amber-600 shrink-0 mt-0.5" />
                  <div>
                    <div className="font-bold text-neutral-900">Official Workshop Email</div>
                    <a
                      href={`mailto:${MOTOR_WORKSHOP_INFO.email}`}
                      className="text-xs font-semibold text-neutral-900 hover:text-amber-700 transition-colors block mt-0.5"
                    >
                      {MOTOR_WORKSHOP_INFO.email}
                    </a>
                    <div className="text-[11px] text-neutral-500 mt-1">
                      Send purchase orders, industrial tender inquiries, or motor data sheets.
                    </div>
                  </div>
                </div>
              </div>

              {/* Operating Hours */}
              <div className="p-4 bg-white rounded-xl border border-neutral-200/90 shadow-sm">
                <div className="flex items-start gap-3">
                  <Clock className="w-5 h-5 text-amber-600 shrink-0 mt-0.5" />
                  <div>
                    <div className="font-bold text-neutral-900">Working Hours</div>
                    <div className="text-xs text-neutral-600 mt-1">
                      {MOTOR_WORKSHOP_INFO.regularHours}
                    </div>
                    <div className="text-[11px] text-amber-800 font-bold mt-1">
                      Emergency agricultural & industrial breakdown support active
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          {/* Right Column: Motor Intake Booking Form */}
          <div className="lg:col-span-7 bg-white rounded-2xl border border-neutral-200 p-6 sm:p-8 shadow-sm">
            {submitted ? (
              <div className="py-10 text-center space-y-5">
                <div className="w-14 h-14 bg-emerald-100 text-emerald-600 rounded-full flex items-center justify-center mx-auto">
                  <CheckCircle2 className="w-8 h-8" />
                </div>

                <div>
                  <div className="text-xs font-bold text-emerald-700 uppercase tracking-wider">
                    Motor Intake Logged
                  </div>
                  <h3 className="text-2xl font-bold text-neutral-900 font-display mt-1">
                    Job Ref: #{ticketId}
                  </h3>
                  <p className="text-sm text-neutral-600 mt-2 max-w-md mx-auto">
                    Thank you, <strong>{formData.name}</strong>. Our head winder will call you at <strong>{formData.phone}</strong> to confirm bench availability or schedule pickup.
                  </p>
                </div>

                <div className="pt-4 flex flex-col sm:flex-row items-center justify-center gap-3">
                  <button
                    onClick={handleWhatsAppSync}
                    className="w-full sm:w-auto px-5 py-2.5 text-xs font-bold text-white bg-emerald-600 hover:bg-emerald-500 rounded-lg flex items-center justify-center gap-2 shadow"
                  >
                    <MessageSquare className="w-4 h-4" />
                    <span>Send Intake Details to WhatsApp ({MOTOR_WORKSHOP_INFO.phonePrimaryRaw})</span>
                  </button>

                  <button
                    onClick={() => {
                      setSubmitted(false);
                      setFormData({
                        name: '',
                        phone: '',
                        location: 'Choondy / Aluva',
                        motorType: 'Submersible Borewell Pump',
                        hpRating: '3.0 HP',
                        problemDesc: '',
                        pickupRequired: false,
                      });
                    }}
                    className="w-full sm:w-auto px-4 py-2.5 text-xs font-semibold text-neutral-700 bg-neutral-100 hover:bg-neutral-200 rounded-lg"
                  >
                    Register Another Motor
                  </button>
                </div>
              </div>
            ) : (
              <form onSubmit={handleSubmit} className="space-y-5">
                <div className="border-b border-neutral-200 pb-3">
                  <h3 className="text-lg font-bold text-neutral-900 font-display">
                    Schedule Motor Drop-off or Pickup
                  </h3>
                  <p className="text-xs text-neutral-500">
                    Bring your motor to our Choondy bench or request on-site transport for heavy industrial pumps.
                  </p>
                </div>

                <div className="grid grid-cols-1 sm:grid-cols-2 gap-4">
                  {/* Name */}
                  <div>
                    <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1.5">
                      Your Name *
                    </label>
                    <input
                      type="text"
                      placeholder="e.g. Joy Joseph"
                      value={formData.name}
                      onChange={(e) => setFormData({ ...formData, name: e.target.value })}
                      className={`w-full px-3.5 py-2.5 text-sm bg-neutral-50 border rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500 ${
                        errors.name ? 'border-red-500 bg-red-50/50' : 'border-neutral-300'
                      }`}
                    />
                    {errors.name && <p className="text-xs text-red-600 mt-1">{errors.name}</p>}
                  </div>

                  {/* Phone */}
                  <div>
                    <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1.5">
                      Mobile Number (WhatsApp) *
                    </label>
                    <input
                      type="tel"
                      placeholder="10-digit mobile"
                      value={formData.phone}
                      onChange={(e) => setFormData({ ...formData, phone: e.target.value })}
                      className={`w-full px-3.5 py-2.5 text-sm bg-neutral-50 border rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500 ${
                        errors.phone ? 'border-red-500 bg-red-50/50' : 'border-neutral-300'
                      }`}
                    />
                    {errors.phone && <p className="text-xs text-red-600 mt-1">{errors.phone}</p>}
                  </div>
                </div>

                <div className="grid grid-cols-1 sm:grid-cols-3 gap-4">
                  {/* Motor Category */}
                  <div>
                    <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1.5">
                      Motor Category
                    </label>
                    <select
                      value={formData.motorType}
                      onChange={(e) => setFormData({ ...formData, motorType: e.target.value })}
                      className="w-full px-3 py-2.5 text-sm bg-neutral-50 border border-neutral-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500"
                    >
                      <option value="Submersible Borewell Pump">Borewell Submersible</option>
                      <option value="3-Phase Induction Stator">3-Phase Industrial Stator</option>
                      <option value="Openwell Submersible Pump">Openwell Pump</option>
                      <option value="Domestic Monobloc Pump">Monobloc Pump</option>
                    </select>
                  </div>

                  {/* HP Capacity */}
                  <div>
                    <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1.5">
                      Power Rating (HP)
                    </label>
                    <select
                      value={formData.hpRating}
                      onChange={(e) => setFormData({ ...formData, hpRating: e.target.value })}
                      className="w-full px-3 py-2.5 text-sm bg-neutral-50 border border-neutral-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500"
                    >
                      <option value="0.5 HP">0.5 HP</option>
                      <option value="1.0 HP">1.0 HP</option>
                      <option value="1.5 HP">1.5 HP</option>
                      <option value="2.0 HP">2.0 HP</option>
                      <option value="3.0 HP">3.0 HP</option>
                      <option value="5.0 HP">5.0 HP</option>
                      <option value="7.5 HP">7.5 HP</option>
                      <option value="10 HP">10 HP</option>
                      <option value="15 HP">15 HP</option>
                      <option value="25 HP+">25 HP or Above</option>
                    </select>
                  </div>

                  {/* Location */}
                  <div>
                    <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1.5">
                      Locality in Aluva *
                    </label>
                    <input
                      type="text"
                      placeholder="e.g. Choondy / Edathala"
                      value={formData.location}
                      onChange={(e) => setFormData({ ...formData, location: e.target.value })}
                      className={`w-full px-3.5 py-2.5 text-sm bg-neutral-50 border rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500 ${
                        errors.location ? 'border-red-500' : 'border-neutral-300'
                      }`}
                    />
                    {errors.location && <p className="text-xs text-red-600 mt-1">{errors.location}</p>}
                  </div>
                </div>

                {/* Pickup checkbox */}
                <label className="flex items-center gap-2.5 p-3 rounded-lg bg-neutral-50 border border-neutral-200 cursor-pointer">
                  <input
                    type="checkbox"
                    checked={formData.pickupRequired}
                    onChange={(e) => setFormData({ ...formData, pickupRequired: e.target.checked })}
                    className="w-4 h-4 rounded text-amber-600 focus:ring-amber-500 border-neutral-300"
                  />
                  <div className="text-xs text-neutral-800">
                    <span className="font-bold">Request Motor Pickup / Transport:</span> Our vehicle can collect heavy motors from your factory or farm in Aluva.
                  </div>
                </label>

                {/* Problem Description */}
                <div>
                  <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1.5">
                    Observed Symptoms (Burnt Smell, Tripping Breaker, Water Leakage)
                  </label>
                  <textarea
                    rows={2}
                    placeholder="e.g. Motor hums but does not spin, or RCCB trips instantly, or pump is making loud grinding noise..."
                    value={formData.problemDesc}
                    onChange={(e) => setFormData({ ...formData, problemDesc: e.target.value })}
                    className="w-full px-3.5 py-2.5 text-sm bg-neutral-50 border border-neutral-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500"
                  />
                </div>

                <button
                  type="submit"
                  className="w-full py-3.5 px-6 text-sm font-bold text-neutral-950 bg-amber-400 hover:bg-amber-300 rounded-lg transition-all shadow hover:shadow-md flex items-center justify-center gap-2 active:scale-[0.98]"
                >
                  <Send className="w-4 h-4" />
                  <span>Submit Motor Intake Request</span>
                </button>
              </form>
            )}
          </div>
        </div>
      </div>
    </section>
  );
};
import React from 'react';
import { Phone, Mail, MapPin, ShieldCheck, Zap, MessageCircle } from 'lucide-react';
import { MOTOR_WORKSHOP_INFO } from '../data/electricalData';

export const Footer: React.FC = () => {
  return (
    <footer className="bg-neutral-950 text-neutral-400 text-xs border-t border-neutral-900 pt-16 pb-12">
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-10 pb-12 border-b border-neutral-900">
          {/* Brand & Purpose */}
          <div className="space-y-4">
            <a href="#" className="text-xl font-extrabold text-white font-display tracking-tight block">
              Excel Electricals
            </a>
            <p className="text-neutral-400 text-xs leading-relaxed">
              Specialized electric motor rewinding and pump overhauling workshop based at Choondy Junction, Aluva. 100% pure electrolytic virgin copper, Nomex Class H slot insulation, and 140°C oven varnish baking.
            </p>
            <div className="flex items-center gap-2 text-neutral-300 text-xs font-semibold">
              <ShieldCheck className="w-4 h-4 text-amber-400" />
              <span>License: {MOTOR_WORKSHOP_INFO.licenseNo}</span>
            </div>
          </div>

          {/* Quick Links */}
          <div className="space-y-3">
            <div className="text-xs font-bold text-white uppercase tracking-wider">
              Motor Services
            </div>
            <ul className="space-y-2">
              {[
                { name: 'Borewell Submersible Rewinding', href: '#services' },
                { name: '3-Phase Industrial Stators', href: '#services' },
                { name: 'Agricultural Monobloc Pumps', href: '#services' },
                { name: 'Winding Gallery & Specs', href: '#gallery' },
                { name: 'Workshop Standards', href: '#workshop' },
              ].map((item) => (
                <li key={item.name}>
                  <a
                    href={item.href}
                    className="hover:text-amber-400 transition-colors"
                  >
                    {item.name}
                  </a>
                </li>
              ))}
            </ul>
          </div>

          {/* Coverage Locations */}
          <div className="space-y-3">
            <div className="text-xs font-bold text-white uppercase tracking-wider">
              Pickup & Drop-off Zones
            </div>
            <div className="text-xs text-neutral-400 leading-relaxed space-y-1">
              <p>Choondy Junction & Bypass</p>
              <p>Aluva Industrial Area & Railway hub</p>
              <p>Edathala & Naval Armament Depot belt</p>
              <p>Perumbavoor Road Timber Belt</p>
              <p>Vazhakkulam & Agricultural Farms</p>
              <p>Kalamassery & Eloor Industrial Zone</p>
            </div>
          </div>

          {/* Direct Contacts */}
          <div className="space-y-3">
            <div className="text-xs font-bold text-white uppercase tracking-wider">
              Workshop Contact
            </div>
            <div className="space-y-2 text-neutral-300">
              <div className="flex items-start gap-2">
                <MapPin className="w-3.5 h-3.5 text-amber-400 shrink-0 mt-0.5" />
                <span>Choondy, Aluva - Perumbavoor Rd, Kerala 683112</span>
              </div>
              <div className="flex items-center gap-2">
                <Phone className="w-3.5 h-3.5 text-amber-400 shrink-0" />
                <a href={`tel:${MOTOR_WORKSHOP_INFO.phonePrimary}`} className="hover:text-white font-bold text-white">
                  {MOTOR_WORKSHOP_INFO.phonePrimary}
                </a>
              </div>
              <div className="flex items-center gap-2">
                <MessageCircle className="w-3.5 h-3.5 text-emerald-400 shrink-0" />
                <a
                  href={`https://wa.me/${MOTOR_WORKSHOP_INFO.phonePrimaryRaw}?text=Hello%20Excel%20Electricals`}
                  target="_blank"
                  rel="noopener noreferrer"
                  className="hover:text-white text-emerald-400 font-semibold"
                >
                  WhatsApp: 85902 59451
                </a>
              </div>
              <div className="flex items-center gap-2">
                <Mail className="w-3.5 h-3.5 text-amber-400 shrink-0" />
                <a href={`mailto:${MOTOR_WORKSHOP_INFO.email}`} className="hover:text-white">
                  {MOTOR_WORKSHOP_INFO.email}
                </a>
              </div>
            </div>
          </div>
        </div>

        {/* Quiet Bottom Legal */}
        <div className="pt-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-[11px] text-neutral-500">
          <div>
            © {new Date().getFullYear()} Excel Electricals Motor Rewinding Workshop, Choondy, Aluva. All rights reserved.
          </div>
          <div className="flex items-center gap-4">
            <span>100% Pure Copper Guarantee</span>
            <span aria-hidden="true">·</span>
            <span>Class H 180°C Insulation</span>
            <span aria-hidden="true">·</span>
            <span>Oven Cured Varnish</span>
          </div>
        </div>
      </div>
    </footer>
  );
};
import React from 'react';
import { X, CheckCircle2, Shield, Clock, Layers, ArrowRight } from 'lucide-react';
import { MotorServiceItem } from '../types';

interface ServiceModalProps {
  service: MotorServiceItem | null;
  onClose: () => void;
  onBookService: (serviceId: string) => void;
}

export const ServiceModal: React.FC<ServiceModalProps> = ({
  service,
  onClose,
  onBookService,
}) => {
  if (!service) return null;

  return (
    <div className="fixed inset-0 z-50 flex items-center justify-center p-4 bg-neutral-950/75 backdrop-blur-sm overflow-y-auto">
      <div 
        className="relative w-full max-w-2xl bg-white rounded-2xl shadow-2xl border border-neutral-200 overflow-hidden my-8 animate-in fade-in zoom-in-95 duration-200"
        role="dialog"
        aria-modal="true"
      >
        {/* Header */}
        <div className="flex items-center justify-between p-6 border-b border-neutral-200">
          <div className="flex items-center gap-2 text-xs font-bold text-amber-700 uppercase tracking-wider">
            <span>Motor Winding Scope</span>
            <span aria-hidden="true">·</span>
            <span>{service.number}</span>
          </div>
          <button
            onClick={onClose}
            className="p-1.5 rounded-lg text-neutral-400 hover:text-neutral-700 hover:bg-neutral-100 transition-colors"
            aria-label="Close modal"
          >
            <X className="w-5 h-5" />
          </button>
        </div>

        {/* Modal Body */}
        <div className="p-6 sm:p-8 space-y-6 max-h-[75vh] overflow-y-auto">
          {/* Photo */}
          <div className="relative aspect-video rounded-xl overflow-hidden bg-neutral-900">
            <img
              src={service.image}
              alt={service.title}
              className="w-full h-full object-cover"
            />
            <div className="absolute inset-0 bg-gradient-to-t from-neutral-950/80 via-transparent to-transparent" />
            <div className="absolute bottom-3 left-4 right-4 flex items-center justify-between text-xs text-white">
              <span className="font-bold text-amber-400">{service.tag}</span>
              <span>{service.turnaroundTime}</span>
            </div>
          </div>

          <div>
            <h3 className="text-2xl font-bold text-neutral-900 font-display mb-2">
              {service.title}
            </h3>
            <p className="text-sm text-neutral-600 leading-relaxed">
              {service.fullDesc}
            </p>
          </div>

          {/* Technical Specifications */}
          <div className="bg-neutral-50 rounded-xl p-5 border border-neutral-200/80">
            <h4 className="text-xs font-bold text-neutral-900 uppercase tracking-wider mb-3">
              Standard Technical Specifications
            </h4>
            <div className="grid grid-cols-1 sm:grid-cols-2 gap-3 text-xs">
              {service.keySpecs.map((spec, idx) => (
                <div key={idx} className="p-2.5 bg-white rounded-lg border border-neutral-200">
                  <div className="text-[10px] text-neutral-400 uppercase font-semibold">{spec.label}</div>
                  <div className="text-neutral-900 font-bold mt-0.5">{spec.value}</div>
                </div>
              ))}
            </div>
          </div>

          {/* Winding Steps */}
          <div>
            <h4 className="text-xs font-bold text-neutral-900 uppercase tracking-wider mb-3">
              Workshop Rewinding Protocol
            </h4>
            <div className="space-y-2">
              {service.processSteps.map((step, idx) => (
                <div key={idx} className="flex items-start gap-2.5 text-xs text-neutral-700">
                  <span className="w-5 h-5 rounded-full bg-amber-100 text-amber-800 flex items-center justify-center font-bold text-[11px] shrink-0 mt-0.5">
                    {idx + 1}
                  </span>
                  <span>{step}</span>
                </div>
              ))}
            </div>
          </div>

          {/* Materials & Guarantee */}
          <div className="grid grid-cols-2 gap-4 text-xs">
            <div className="p-4 rounded-xl border border-neutral-200 bg-white">
              <div className="flex items-center gap-1.5 text-neutral-500 font-semibold mb-1">
                <Shield className="w-3.5 h-3.5 text-amber-600" />
                <span>Warranty</span>
              </div>
              <div className="font-bold text-neutral-900">{service.warranty}</div>
            </div>

            <div className="p-4 rounded-xl border border-neutral-200 bg-white">
              <div className="flex items-center gap-1.5 text-neutral-500 font-semibold mb-1">
                <Clock className="w-3.5 h-3.5 text-amber-600" />
                <span>Turnaround Time</span>
              </div>
              <div className="font-bold text-neutral-900">{service.turnaroundTime}</div>
            </div>
          </div>
        </div>

        {/* Footer Actions */}
        <div className="p-6 bg-neutral-50 border-t border-neutral-200 flex flex-col sm:flex-row items-center justify-between gap-3">
          <button
            onClick={onClose}
            className="w-full sm:w-auto px-4 py-2.5 text-xs font-semibold text-neutral-700 hover:text-neutral-900 transition-colors"
          >
            Close Details
          </button>

          <button
            onClick={() => {
              onClose();
              onBookService(service.id);
            }}
            className="w-full sm:w-auto px-6 py-2.5 text-xs font-bold text-neutral-950 bg-amber-400 hover:bg-amber-300 rounded-lg shadow-sm transition-all flex items-center justify-center gap-1.5"
          >
            <span>Book This Motor Rewind</span>
            <ArrowRight className="w-3.5 h-3.5" />
          </button>
        </div>
      </div>
    </div>
  );
};
import React from 'react';
import { X, Zap, ArrowRight, ShieldCheck, CheckCircle2 } from 'lucide-react';
import { MotorJobItem } from '../types';
import { MOTOR_WORKSHOP_INFO } from '../data/electricalData';

interface ProjectModalProps {
  project: MotorJobItem | null;
  onClose: () => void;
  onInquireSimilar: (projectTitle: string) => void;
}

export const ProjectModal: React.FC<ProjectModalProps> = ({
  project,
  onClose,
  onInquireSimilar,
}) => {
  if (!project) return null;

  return (
    <div className="fixed inset-0 z-50 flex items-center justify-center p-4 bg-neutral-950/75 backdrop-blur-sm overflow-y-auto">
      <div 
        className="relative w-full max-w-2xl bg-white rounded-2xl shadow-2xl border border-neutral-200 overflow-hidden my-8 animate-in fade-in zoom-in-95 duration-200"
        role="dialog"
        aria-modal="true"
      >
        {/* Header */}
        <div className="flex items-center justify-between p-6 border-b border-neutral-200">
          <div className="flex items-center gap-2 text-xs font-bold text-amber-700 uppercase tracking-wider">
            <span>Motor Winding Job Record</span>
            <span aria-hidden="true">·</span>
            <span>{project.capacity}</span>
          </div>
          <button
            onClick={onClose}
            className="p-1.5 rounded-lg text-neutral-400 hover:text-neutral-700 hover:bg-neutral-100 transition-colors"
            aria-label="Close modal"
          >
            <X className="w-5 h-5" />
          </button>
        </div>

        {/* Modal Body */}
        <div className="p-6 sm:p-8 space-y-6 max-h-[75vh] overflow-y-auto">
          {/* Main Visual */}
          <div className="relative aspect-video rounded-xl overflow-hidden bg-neutral-900">
            <img
              src={project.image}
              alt={project.title}
              className="w-full h-full object-cover"
            />
            <div className="absolute inset-0 bg-gradient-to-t from-neutral-950/80 via-transparent to-transparent" />
            <div className="absolute bottom-4 left-4 right-4 flex items-center justify-between text-xs text-white">
              <span className="font-bold text-amber-400">{project.capacity}</span>
              <span className="text-neutral-300">{project.client}</span>
            </div>
          </div>

          <div>
            <h3 className="text-2xl font-bold text-neutral-900 font-display mb-2">
              {project.title}
            </h3>
            <p className="text-sm text-neutral-600 leading-relaxed">
              {project.description}
            </p>
          </div>

          {/* Deep Winding Specifications Table */}
          <div className="bg-neutral-50 rounded-xl p-5 border border-neutral-200/80">
            <h4 className="text-xs font-bold text-neutral-900 uppercase tracking-wider mb-3">
              Recorded Winding Data & Electrical Test Results
            </h4>
            <div className="grid grid-cols-2 gap-3 text-xs">
              <div className="p-2.5 bg-white rounded-lg border border-neutral-200">
                <span className="text-[10px] text-neutral-400 font-semibold uppercase block">Horsepower / Voltage</span>
                <span className="font-bold text-neutral-800 text-[11px]">{project.technicalSpecs.hpRating}</span>
              </div>
              <div className="p-2.5 bg-white rounded-lg border border-neutral-200">
                <span className="text-[10px] text-neutral-400 font-semibold uppercase block">Phase Connection</span>
                <span className="font-bold text-neutral-800 text-[11px]">{project.technicalSpecs.phase}</span>
              </div>
              <div className="p-2.5 bg-white rounded-lg border border-neutral-200">
                <span className="text-[10px] text-neutral-400 font-semibold uppercase block">Poles & Speed (RPM)</span>
                <span className="font-bold text-neutral-800 text-[11px]">{project.technicalSpecs.polesRpm}</span>
              </div>
              <div className="p-2.5 bg-white rounded-lg border border-neutral-200">
                <span className="text-[10px] text-neutral-400 font-semibold uppercase block">Slot Count & Coil Pitch</span>
                <span className="font-bold text-neutral-800 text-[11px]">{project.technicalSpecs.slotCount}</span>
              </div>
              <div className="p-2.5 bg-white rounded-lg border border-neutral-200">
                <span className="text-[10px] text-neutral-400 font-semibold uppercase block">Copper Wire Gauge (SWG)</span>
                <span className="font-bold text-neutral-800 text-[11px]">{project.technicalSpecs.wireSwg}</span>
              </div>
              <div className="p-2.5 bg-white rounded-lg border border-neutral-200">
                <span className="text-[10px] text-neutral-400 font-semibold uppercase block">Slot Liner Insulation</span>
                <span className="font-bold text-neutral-800 text-[11px]">{project.technicalSpecs.insulation}</span>
              </div>
              <div className="p-2.5 bg-white rounded-lg border border-neutral-200">
                <span className="text-[10px] text-neutral-400 font-semibold uppercase block">Varnish & Oven Curing</span>
                <span className="font-bold text-neutral-800 text-[11px]">{project.technicalSpecs.varnishBaking}</span>
              </div>
              <div className="p-2.5 bg-white rounded-lg border border-neutral-200">
                <span className="text-[10px] text-neutral-400 font-semibold uppercase block">Insulation Resistance (Megger)</span>
                <span className="font-bold text-emerald-700 text-[11px]">{project.technicalSpecs.meggerReading}</span>
              </div>
            </div>
          </div>

          {/* Faults Resolved */}
          <div>
            <h4 className="text-xs font-bold text-neutral-900 uppercase tracking-wider mb-2">
              Defects Repaired & Restored
            </h4>
            <div className="space-y-1.5 text-xs text-neutral-700">
              {project.symptomsResolved.map((symp, idx) => (
                <div key={idx} className="flex items-start gap-2">
                  <CheckCircle2 className="w-4 h-4 text-emerald-600 shrink-0 mt-0.5" />
                  <span>{symp}</span>
                </div>
              ))}
            </div>
          </div>
        </div>

        {/* Footer Actions */}
        <div className="p-6 bg-neutral-50 border-t border-neutral-200 flex flex-col sm:flex-row items-center justify-between gap-3">
          <button
            onClick={onClose}
            className="w-full sm:w-auto px-4 py-2.5 text-xs font-semibold text-neutral-700 hover:text-neutral-900 transition-colors"
          >
            Close
          </button>

          <button
            onClick={() => {
              onClose();
              onInquireSimilar(project.title);
            }}
            className="w-full sm:w-auto px-6 py-2.5 text-xs font-bold text-neutral-950 bg-amber-400 hover:bg-amber-300 rounded-lg shadow-sm transition-all flex items-center justify-center gap-1.5"
          >
            <span>Inquire Similar Motor Rewind</span>
            <ArrowRight className="w-3.5 h-3.5" />
          </button>
        </div>
      </div>
    </div>
  );
};
import React, { useState } from 'react';
import { X, Send, CheckCircle2, MessageSquare, Phone, Wrench } from 'lucide-react';
import { MOTOR_WORKSHOP_INFO, MOTOR_SERVICES_DATA } from '../data/electricalData';

interface QuoteModalProps {
  isOpen: boolean;
  onClose: () => void;
  defaultService?: string;
  defaultNotes?: string;
}

export const QuoteModal: React.FC<QuoteModalProps> = ({
  isOpen,
  onClose,
  defaultService = 'submersible-borewell-rewinding',
  defaultNotes = '',
}) => {
  const [name, setName] = useState('');
  const [phone, setPhone] = useState('');
  const [service, setService] = useState(defaultService);
  const [hp, setHp] = useState('3.0 HP');
  const [location, setLocation] = useState('Choondy / Aluva');
  const [notes, setNotes] = useState(defaultNotes);
  const [errors, setErrors] = useState<Record<string, string>>({});
  const [isSuccess, setIsSuccess] = useState(false);
  const [ticketId, setTicketId] = useState('');

  if (!isOpen) return null;

  const validate = () => {
    const errs: Record<string, string> = {};
    if (!name.trim()) errs.name = 'Please provide your name.';
    const clean = phone.replace(/[\s-+()]/g, '');
    if (!clean || clean.length < 10) errs.phone = 'Valid 10-digit number required.';
    if (!location.trim()) errs.location = 'Please mention your locality in Aluva.';
    setErrors(errs);
    return Object.keys(errs).length === 0;
  };

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    if (!validate()) return;
    const ref = `MOT-${Math.floor(100000 + Math.random() * 900000)}`;
    setTicketId(ref);
    setIsSuccess(true);
  };

  const handleWhatsApp = () => {
    const sName = MOTOR_SERVICES_DATA.find((s) => s.id === service)?.title || service;
    const text = `*New Motor Rewind Inquiry [${ticketId}]*%0A` +
      `• *Name:* ${encodeURIComponent(name)}%0A` +
      `• *Phone:* ${encodeURIComponent(phone)}%0A` +
      `• *Location:* ${encodeURIComponent(location)}%0A` +
      `• *Motor Type:* ${encodeURIComponent(sName)}%0A` +
      `• *Capacity:* ${encodeURIComponent(hp)}%0A` +
      `• *Details:* ${encodeURIComponent(notes || 'Rewinding consultation requested')}`;
    window.open(`https://wa.me/${MOTOR_WORKSHOP_INFO.phonePrimaryRaw}?text=${text}`, '_blank');
  };

  return (
    <div className="fixed inset-0 z-50 flex items-center justify-center p-4 bg-neutral-950/75 backdrop-blur-sm overflow-y-auto">
      <div 
        className="relative w-full max-w-lg bg-white rounded-2xl shadow-2xl border border-neutral-200 overflow-hidden my-8 animate-in fade-in zoom-in-95 duration-200"
        role="dialog"
        aria-modal="true"
      >
        <div className="flex items-center justify-between p-6 border-b border-neutral-200 bg-neutral-50">
          <div>
            <div className="text-xs font-bold text-amber-700 uppercase tracking-wider">
              Excel Electricals · Choondy, Aluva
            </div>
            <h3 className="text-lg font-bold text-neutral-900 font-display">
              Book Motor Drop-Off / Fast-Track Rewind
            </h3>
          </div>
          <button
            onClick={onClose}
            className="p-1.5 rounded-lg text-neutral-400 hover:text-neutral-700 hover:bg-neutral-200 transition-colors"
          >
            <X className="w-5 h-5" />
          </button>
        </div>

        <div className="p-6">
          {isSuccess ? (
            <div className="py-6 text-center space-y-4">
              <div className="w-12 h-12 bg-emerald-100 text-emerald-600 rounded-full flex items-center justify-center mx-auto">
                <CheckCircle2 className="w-7 h-7" />
              </div>
              <h4 className="text-xl font-bold text-neutral-900 font-display">
                Intake Logged: #{ticketId}
              </h4>
              <p className="text-xs text-neutral-600 max-w-xs mx-auto">
                Our head technician will contact you at <strong>{phone}</strong> to confirm bench scheduling and drop-off instructions at Choondy Junction.
              </p>
              <div className="pt-2 flex flex-col gap-2">
                <button
                  onClick={handleWhatsApp}
                  className="w-full py-2.5 px-4 text-xs font-bold text-white bg-emerald-600 hover:bg-emerald-500 rounded-lg flex items-center justify-center gap-2"
                >
                  <MessageSquare className="w-4 h-4" />
                  <span>Send to WhatsApp (85902 59451)</span>
                </button>
                <button
                  onClick={onClose}
                  className="w-full py-2 px-4 text-xs font-semibold text-neutral-700 hover:bg-neutral-100 rounded-lg"
                >
                  Close
                </button>
              </div>
            </div>
          ) : (
            <form onSubmit={handleSubmit} className="space-y-4">
              <div>
                <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1">
                  Your Full Name *
                </label>
                <input
                  type="text"
                  placeholder="e.g. Salim Ali"
                  value={name}
                  onChange={(e) => setName(e.target.value)}
                  className={`w-full px-3 py-2 text-sm bg-neutral-50 border rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500 ${
                    errors.name ? 'border-red-500' : 'border-neutral-300'
                  }`}
                />
                {errors.name && <p className="text-xs text-red-600 mt-1">{errors.name}</p>}
              </div>

              <div className="grid grid-cols-2 gap-3">
                <div>
                  <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1">
                    Mobile Phone *
                  </label>
                  <input
                    type="tel"
                    placeholder="10-digit mobile"
                    value={phone}
                    onChange={(e) => setPhone(e.target.value)}
                    className={`w-full px-3 py-2 text-sm bg-neutral-50 border rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500 ${
                      errors.phone ? 'border-red-500' : 'border-neutral-300'
                    }`}
                  />
                  {errors.phone && <p className="text-xs text-red-600 mt-1">{errors.phone}</p>}
                </div>

                <div>
                  <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1">
                    Locality in Aluva *
                  </label>
                  <input
                    type="text"
                    placeholder="e.g. Choondy / Edathala"
                    value={location}
                    onChange={(e) => setLocation(e.target.value)}
                    className={`w-full px-3 py-2 text-sm bg-neutral-50 border rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500 ${
                      errors.location ? 'border-red-500' : 'border-neutral-300'
                    }`}
                  />
                  {errors.location && <p className="text-xs text-red-600 mt-1">{errors.location}</p>}
                </div>
              </div>

              <div className="grid grid-cols-2 gap-3">
                <div>
                  <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1">
                    Motor Type
                  </label>
                  <select
                    value={service}
                    onChange={(e) => setService(e.target.value)}
                    className="w-full px-3 py-2 text-sm bg-neutral-50 border border-neutral-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500"
                  >
                    {MOTOR_SERVICES_DATA.map((srv) => (
                      <option key={srv.id} value={srv.id}>
                        {srv.number}. {srv.tag}
                      </option>
                    ))}
                  </select>
                </div>

                <div>
                  <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1">
                    Power (HP)
                  </label>
                  <select
                    value={hp}
                    onChange={(e) => setHp(e.target.value)}
                    className="w-full px-3 py-2 text-sm bg-neutral-50 border border-neutral-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500"
                  >
                    <option value="0.5 HP">0.5 HP</option>
                    <option value="1.0 HP">1.0 HP</option>
                    <option value="2.0 HP">2.0 HP</option>
                    <option value="3.0 HP">3.0 HP</option>
                    <option value="5.0 HP">5.0 HP</option>
                    <option value="7.5 HP">7.5 HP</option>
                    <option value="10 HP">10 HP</option>
                    <option value="15 HP+">15 HP or more</option>
                  </select>
                </div>
              </div>

              <div>
                <label className="block text-xs font-bold text-neutral-700 uppercase tracking-wider mb-1">
                  Symptoms / Fault Details (Optional)
                </label>
                <textarea
                  rows={2}
                  placeholder="e.g. Pump tripped breaker, or burnt smell, or shaft seized..."
                  value={notes}
                  onChange={(e) => setNotes(e.target.value)}
                  className="w-full px-3 py-2 text-sm bg-neutral-50 border border-neutral-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-500"
                />
              </div>

              <div className="pt-2">
                <button
                  type="submit"
                  className="w-full py-3 px-4 text-xs font-bold text-neutral-950 bg-amber-400 hover:bg-amber-300 rounded-lg shadow transition-all flex items-center justify-center gap-1.5"
                >
                  <Send className="w-3.5 h-3.5" />
                  <span>Submit Motor Booking</span>
                </button>
              </div>
            </form>
          )}
        </div>
      </div>
    </div>
  );
};
/**
 * @license
 * SPDX-License-Identifier: Apache-2.0
 */

import React, { useState } from 'react';
import { Navbar } from './components/Navbar';
import { Hero } from './components/Hero';
import { MotorPhotosShowcase } from './components/MotorPhotosShowcase';
import { ServicesSection } from './components/ServicesSection';
import { ProjectsSection } from './components/ProjectsSection';
import { EmergencySection } from './components/EmergencySection';
import { BrandsSection } from './components/BrandsSection';
import { TestimonialsSection } from './components/TestimonialsSection';
import { ContactSection } from './components/ContactSection';
import { Footer } from './components/Footer';
import { ServiceModal } from './components/ServiceModal';
import { ProjectModal } from './components/ProjectModal';
import { QuoteModal } from './components/QuoteModal';
import { MotorServiceItem, MotorJobItem } from './types';
import { Phone, MessageCircle } from 'lucide-react';
import { MOTOR_WORKSHOP_INFO } from './data/electricalData';

export default function App() {
  const [selectedService, setSelectedService] = useState<MotorServiceItem | null>(null);
  const [selectedProject, setSelectedProject] = useState<MotorJobItem | null>(null);
  const [quoteModalOpen, setQuoteModalOpen] = useState(false);
  const [quotePrefillService, setQuotePrefillService] = useState<string>('submersible-borewell-rewinding');
  const [quotePrefillNotes, setQuotePrefillNotes] = useState<string>('');

  const handleOpenBooking = (serviceId?: string, notes?: string) => {
    if (serviceId) setQuotePrefillService(serviceId);
    if (notes) setQuotePrefillNotes(notes);
    setQuoteModalOpen(true);
  };

  const handleScrollToContact = () => {
    const el = document.getElementById('contact');
    if (el) {
      el.scrollIntoView({ behavior: 'smooth' });
    }
  };

  const handleInquireSimilarProject = (projectTitle: string) => {
    handleOpenBooking('three-phase-induction-rewinding', `Inquiry regarding motor rewinding similar to: ${projectTitle}`);
  };

  return (
    <div className="min-h-screen flex flex-col bg-neutral-50 text-neutral-900 selection:bg-amber-400 selection:text-neutral-950 font-sans">
      {/* Top Bar Navigation */}
      <Navbar onOpenBooking={() => handleOpenBooking()} />

      <main className="flex-1">
        {/* Hero Section */}
        <Hero
          onOpenBooking={() => handleOpenBooking()}
          onScrollToContact={handleScrollToContact}
        />

        {/* Dedicated Motor Winding Photos Gallery Showcase */}
        <MotorPhotosShowcase
          onOpenBooking={() => handleOpenBooking()}
        />

        {/* Core Motor Winding Capabilities */}
        <ServicesSection
          onSelectService={(service) => setSelectedService(service)}
          onOpenBookingWithService={(serviceId) => handleOpenBooking(serviceId)}
        />

        {/* Real Winding Gallery & Technical Case Studies */}
        <ProjectsSection
          onSelectProject={(project) => setSelectedProject(project)}
        />

        {/* Motor Breakdown & Urgent Pump Failure Protocol */}
        <EmergencySection />

        {/* Workshop Quality Standards & Pure Copper Guarantee */}
        <BrandsSection />

        {/* Attributable Client Reviews & Winding FAQs */}
        <TestimonialsSection />

        {/* Workshop Drop-off & Motor Intake Form */}
        <ContactSection
          prefilledService={quotePrefillService}
          prefilledNote={quotePrefillNotes}
        />
      </main>

      {/* Quiet Footer */}
      <Footer />

      {/* Floating Bottom Quick-Action Bar for Mobile (Height ≤ 44px) */}
      <div className="sm:hidden fixed bottom-0 left-0 right-0 z-40 bg-neutral-950/95 backdrop-blur-md border-t border-neutral-800 px-3 py-2 flex items-center justify-between gap-2 shadow-2xl">
        <a
          href={`tel:${MOTOR_WORKSHOP_INFO.phonePrimary}`}
          className="flex-1 py-2 px-3 text-xs font-bold text-neutral-950 bg-amber-400 rounded-lg flex items-center justify-center gap-1.5 active:scale-95 transition-transform"
        >
          <Phone className="w-3.5 h-3.5 fill-neutral-950" />
          <span>Call 85902 59451</span>
        </a>
        <a
          href={`https://wa.me/${MOTOR_WORKSHOP_INFO.phonePrimaryRaw}?text=Hello%20Excel%20Electricals%20Choondy,%20I%20have%20an%20urgent%20motor%20winding%20inquiry.`}
          target="_blank"
          rel="noopener noreferrer"
          className="flex-1 py-2 px-3 text-xs font-bold text-white bg-emerald-600 rounded-lg flex items-center justify-center gap-1.5 active:scale-95 transition-transform"
        >
          <MessageCircle className="w-3.5 h-3.5" />
          <span>WhatsApp 85902 59451</span>
        </a>
      </div>

      {/* Interactive Modals */}
      <ServiceModal
        service={selectedService}
        onClose={() => setSelectedService(null)}
        onBookService={(serviceId) => handleOpenBooking(serviceId)}
      />

      <ProjectModal
        project={selectedProject}
        onClose={() => setSelectedProject(null)}
        onInquireSimilar={handleInquireSimilarProject}
      />

      <QuoteModal
        isOpen={quoteModalOpen}
        onClose={() => setQuoteModalOpen(false)}
        defaultService={quotePrefillService}
        defaultNotes={quotePrefillNotes}
      />
    </div>
  );
}
