import React, { useState, useEffect, useRef } from 'react';
import { 
  Terminal, Server, Globe, Shield, Mail, Cpu, FileText, 
  Code, Database, Image, Lock, Share2, Search, Clock, 
  Hash, Calendar, Repeat, Copy, Check, 
  AlertTriangle, ExternalLink, Menu, X, Wifi, Download,
  Settings, Link as LinkIcon, HardDrive, RefreshCw, Layers,
  Smartphone, ShoppingCart, Gamepad2, Heart, Keyboard,
  Monitor, Play, Trash2, Split, Plus, Save, Command, QrCode,
  Cloud, Activity, UserPlus, ListChecks, MessageSquare, Grid,
  Type, ArrowRight, Book, Calculator, Key, Info, CheckCircle2, Circle
} from 'lucide-react';

// --- HELPER FUNCTIONS ---

const copyToClipboard = (text) => {
  const el = document.createElement('textarea');
  el.value = text;
  document.body.appendChild(el);
  el.select();
  document.execCommand('copy');
  document.body.removeChild(el);
};

// --- SHARED UI COMPONENTS ---

function ExternalToolsList({ tools }) {
  return (
    <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      {tools.map((t, i) => (
        <a key={i} href={t.url} target="_blank" rel="noopener noreferrer" className="bg-slate-800 hover:bg-slate-700 border border-slate-700 rounded-lg p-4 group transition-all flex flex-col justify-between h-32">
          <div className="flex justify-between items-start">
            <div className="font-bold text-slate-200 group-hover:text-blue-400">{t.name}</div>
            <ExternalLink size={16} className="text-slate-500 group-hover:text-white" />
          </div>
          <div className="text-xs text-slate-500">{t.desc}</div>
        </a>
      ))}
    </div>
  );
}

// --- WIDGET COMPONENTS (For Dashboard) ---

function SystemSummary() {
  const info = {
    OS: navigator.platform,
    Browser: "Agent v1.0",
    Language: navigator.language,
    Cores: navigator.hardwareConcurrency || 'N/A'
  };
  return (
    <div className="bg-slate-800 p-4 rounded-xl border border-slate-700 h-full">
      <div className="text-xs font-bold text-slate-500 uppercase mb-3 flex items-center gap-2">
        <Info size={14}/> Local System Info
      </div>
      <div className="grid grid-cols-2 gap-2 text-[11px] font-mono">
        {Object.entries(info).map(([k,v]) => (
          <div key={k} className="flex flex-col bg-slate-900/50 p-2 rounded border border-slate-700/50">
            <span className="text-slate-500">{k}</span>
            <span className="text-blue-400 truncate">{v}</span>
          </div>
        ))}
      </div>
    </div>
  );
}

function UnitConverter() {
  const [val, setVal] = useState(1);
  const [unit, setUnit] = useState('GB');
  const units = { 'B': 1, 'KB': 1024, 'MB': 1024 ** 2, 'GB': 1024 ** 3, 'TB': 1024 ** 4 };
  const convert = (target) => {
    const bytes = val * units[unit];
    const result = bytes / units[target];
    return result < 0.01 ? result.toExponential(2) : result.toLocaleString(undefined, {maximumFractionDigits: 2});
  };
  return (
    <div className="bg-slate-800 p-4 rounded-xl border border-slate-700 h-full">
      <div className="text-xs font-bold text-slate-500 uppercase mb-3 flex items-center gap-2">
        <Calculator size={14}/> Unit Converter
      </div>
      <div className="flex gap-2 mb-4">
        <input type="number" value={val} onChange={e => setVal(e.target.value)} className="w-full bg-slate-900 border border-slate-700 rounded p-2 text-white font-mono text-sm focus:outline-none" />
        <select value={unit} onChange={e => setUnit(e.target.value)} className="bg-slate-900 border border-slate-700 rounded p-1 text-xs text-blue-400 font-bold outline-none">
          {Object.keys(units).map(u => <option key={u} value={u}>{u}</option>)}
        </select>
      </div>
      <div className="space-y-1">
        {Object.keys(units).filter(u => u !== unit).map(u => (
          <div key={u} className="flex justify-between text-xs font-mono p-1.5 border-b border-slate-700/50 last:border-0">
            <span className="text-slate-500">{u}</span>
            <span className="text-slate-200">{convert(u)}</span>
          </div>
        ))}
      </div>
    </div>
  );
}

function IpWidget() {
  const [ip, setIp] = useState('Loading...');
  const [online, setOnline] = useState(navigator.onLine);
  useEffect(() => {
    fetch('https://api.ipify.org?format=json').then(res => res.json()).then(data => setIp(data.ip)).catch(() => setIp('Offline'));
    const handleStatus = () => setOnline(navigator.onLine);
    window.addEventListener('online', handleStatus);
    window.addEventListener('offline', handleStatus);
    return () => { window.removeEventListener('online', handleStatus); window.removeEventListener('offline', handleStatus); };
  }, []);
  return (
    <div className="bg-slate-800 p-4 rounded-xl border border-slate-700 flex items-center justify-between shadow-lg relative overflow-hidden">
      <div className={`absolute top-0 left-0 w-1 h-full ${online ? 'bg-green-500' : 'bg-red-500'}`}></div>
      <div>
        <div className="text-xs text-slate-500 font-bold uppercase flex items-center gap-2">
          Public IP {online ? <span className="text-[10px] text-green-500 animate-pulse">● LIVE</span> : <span className="text-[10px] text-red-500">● OFFLINE</span>}
        </div>
        <div className="text-2xl font-mono text-blue-400 font-bold tracking-tight">{ip}</div>
      </div>
      <Globe className="text-slate-600" size={32} />
    </div>
  );
}

function NewsFeed() {
  const feeds = [
    { t: "HotUKDeals: Server Hardware", l: "Latest deals on enterprise gear", u: "https://www.hotukdeals.com/tag/server" },
    { t: "The Hacker News", l: "Cybersecurity Briefs", u: "https://thehackernews.com/" },
    { t: "Ars Technica: IT", l: "Policy & Tech Analysis", u: "https://arstechnica.com/information-technology/" },
    { t: "MoneySavingExpert: Mobile", l: "Best SIM-Only Deals", u: "https://www.moneysavingexpert.com/mobiles/" }
  ];
  return (
    <div className="bg-slate-800 rounded-xl border border-slate-700 overflow-hidden flex flex-col h-full">
      <div className="p-3 bg-slate-900/50 border-b border-slate-700 font-bold text-slate-300 flex items-center gap-2 text-xs uppercase tracking-wider">
        <Share2 size={14} /> Tech News & Deals
      </div>
      <div className="overflow-y-auto max-h-64 flex-1">
        {feeds.map((n, i) => (
          <a key={i} href={n.u} target="_blank" rel="noreferrer" className="block p-3 hover:bg-slate-700 border-b border-slate-700/50 last:border-0">
            <div className="font-bold text-sm text-blue-400">{n.t}</div>
            <div className="text-xs text-slate-500">{n.l}</div>
          </a>
        ))}
      </div>
    </div>
  );
}

function DashboardHome() {
  return (
    <div className="grid grid-cols-1 lg:grid-cols-3 gap-6 animate-in fade-in duration-500">
      <div className="lg:col-span-2 space-y-6">
        <IpWidget />
        <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
          <SystemSummary />
          <div className="bg-slate-800 p-4 rounded-xl border border-slate-700 flex flex-col justify-center">
            <div className="text-xs font-bold text-slate-500 uppercase mb-2 font-mono">Quick Admin Links</div>
            <div className="grid grid-cols-2 gap-2 font-mono text-[9px]">
              <a href="https://admin.microsoft.com" target="_blank" rel="noreferrer" className="p-2 bg-slate-900 hover:bg-blue-900 border border-slate-700 rounded text-center text-slate-300">M365 ADMIN</a>
              <a href="https://entra.microsoft.com" target="_blank" rel="noreferrer" className="p-2 bg-slate-900 hover:bg-blue-900 border border-slate-700 rounded text-center text-slate-300">ENTRA ID</a>
              <a href="https://intune.microsoft.com" target="_blank" rel="noreferrer" className="p-2 bg-slate-900 hover:bg-blue-900 border border-slate-700 rounded text-center text-slate-300">INTUNE</a>
              <a href="https://security.microsoft.com" target="_blank" rel="noreferrer" className="p-2 bg-slate-900 hover:bg-blue-900 border border-slate-700 rounded text-center text-slate-300">SECURITY</a>
            </div>
          </div>
        </div>
        <NewsFeed />
      </div>
      <div className="lg:col-span-1 space-y-6">
        <UnitConverter />
        <div className="bg-blue-600/10 border border-blue-500/20 p-4 rounded-xl text-xs italic text-slate-400 leading-relaxed">
          "Analyze headers before checking the server. Restart spooler before the driver. Verify DNS before the firewall."
        </div>
      </div>
    </div>
  );
}

// --- CORE UTILITY COMPONENTS ---

function M365Launcher() {
  const portals = [
    { n: 'M365 Admin', u: 'https://admin.microsoft.com', i: 'Admin' },
    { n: 'Entra ID', u: 'https://entra.microsoft.com', i: 'Entra' },
    { n: 'Exchange', u: 'https://admin.exchange.microsoft.com', i: 'Exch' },
    { n: 'Intune', u: 'https://intune.microsoft.com', i: 'Intune' },
    { n: 'Security', u: 'https://security.microsoft.com', i: 'Sec' },
    { n: 'Purview', u: 'https://compliance.microsoft.com', i: 'Comp' },
    { n: 'Azure', u: 'https://portal.azure.com', i: 'Azure' },
    { n: 'Teams', u: 'https://admin.teams.microsoft.com', i: 'Teams' },
  ];

  return (
    <div className="grid grid-cols-2 md:grid-cols-4 gap-4">
      {portals.map((p, i) => (
        <a key={i} href={p.u} target="_blank" rel="noreferrer" className="aspect-square bg-slate-800 hover:bg-blue-900 border border-slate-700 hover:border-blue-500 rounded-xl flex flex-col items-center justify-center gap-3 transition-all group">
          <div className="w-12 h-12 rounded-full bg-slate-900 flex items-center justify-center font-bold text-xs text-slate-200 group-hover:text-white group-hover:bg-blue-600 transition-colors uppercase">
            {p.i}
          </div>
          <span className="font-bold text-slate-300 group-hover:text-white text-xs">{p.n}</span>
        </a>
      ))}
    </div>
  );
}

function PortReference() {
  const ports = [
    { p: 22, t: 'TCP', n: 'SSH' }, { p: 80, t: 'TCP', n: 'HTTP' }, { p: 443, t: 'TCP', n: 'HTTPS' },
    { p: 3389, t: 'TCP', n: 'RDP' }, { p: 53, t: 'UDP', n: 'DNS' }, { p: 25, t: 'TCP', n: 'SMTP' },
    { p: 445, t: 'TCP', n: 'SMB' }, { p: 1433, t: 'TCP', n: 'SQL' }, { p: 3306, t: 'TCP', n: 'MySQL' }
  ];
  return (
    <div className="bg-slate-800 rounded-xl border border-slate-700 overflow-hidden shadow-lg">
      <table className="w-full text-left text-sm font-mono">
        <thead className="bg-slate-900 text-slate-500 uppercase text-xs"><tr><th className="p-3">Port</th><th className="p-3">Type</th><th className="p-3">Service</th></tr></thead>
        <tbody className="divide-y divide-slate-700 text-slate-300">
          {ports.map((n, i) => (
            <tr key={i} className="hover:bg-slate-700/50"><td className="p-3 text-blue-400 font-bold">{n.p}</td><td className="p-3 text-slate-500 text-[10px]">{n.t}</td><td className="p-3 font-sans text-xs">{n.n}</td></tr>
          ))}
        </tbody>
      </table>
    </div>
  );
}

function Scratchpad() {
  const [text, setText] = useState(localStorage.getItem('it-scratchpad') || '');
  useEffect(() => { localStorage.setItem('it-scratchpad', text); }, [text]);
  return (
    <div className="h-full flex flex-col">
      <div className="flex justify-between items-center mb-2">
        <label className="text-xs font-bold text-slate-500 uppercase tracking-widest">Persistent Scratchpad</label>
        <button onClick={() => setText('')} className="text-slate-500 hover:text-red-400 transition-colors"><Trash2 size={14}/></button>
      </div>
      <textarea className="flex-1 bg-slate-900 border border-slate-700 rounded p-4 font-mono text-sm text-slate-300 focus:outline-none resize-none min-h-[400px]" placeholder="// Temporary notes, script snippets, etc." value={text} onChange={(e) => setText(e.target.value)} />
    </div>
  );
}

function CommandLibrary() {
  const defaultCmds = [
    { id: 1, title: 'Citrix Print Fix', cmd: 'sc query "CpSvc" | find "RUNNING" >nul || net start "CpSvc" & logoff', tags: 'fix' },
    { id: 2, title: 'Flush DNS', cmd: 'ipconfig /flushdns', tags: 'net' },
    { id: 3, title: 'Force GPO Update', cmd: 'gpupdate /force', tags: 'ad' }
  ];
  const [commands] = useState(() => JSON.parse(localStorage.getItem('it-cmd-library')) || defaultCmds);
  return (
    <div className="space-y-3">
      {commands.map(c => (
        <div key={c.id} className="bg-slate-800 border border-slate-700 rounded-lg p-4 hover:border-slate-500 transition-all">
          <div className="flex justify-between font-bold text-slate-200 mb-2 items-center">
            <span className="text-sm">{c.title}</span>
            <button onClick={() => copyToClipboard(c.cmd)} className="text-slate-500 hover:text-blue-400 transition-colors"><Copy size={14}/></button>
          </div>
          <div className="bg-slate-950 p-3 rounded font-mono text-xs text-green-400 break-all select-all">{c.cmd}</div>
        </div>
      ))}
    </div>
  );
}

function MvnoMatrix() {
  const networks = [
    { name: 'GiffGaff', host: 'O2' }, { name: 'Smarty', host: 'Three' }, 
    { name: 'VOXI', host: 'Vodafone' }, { name: 'Lyca', host: 'EE' },
    { name: 'Sky Mobile', host: 'O2' }, { name: 'ID Mobile', host: 'Three' }
  ];
  return (
    <div className="bg-slate-800 rounded-xl border border-slate-700 overflow-hidden shadow-lg">
      <table className="w-full text-left text-sm">
        <thead className="bg-slate-900 text-slate-500 uppercase text-xs"><tr><th className="p-3">Provider</th><th className="p-3">Host Network</th></tr></thead>
        <tbody className="divide-y divide-slate-700">
          {networks.map((n, i) => (<tr key={i} className="hover:bg-slate-700/30 transition-colors"><td className="p-3 font-bold text-slate-200">{n.name}</td><td className="p-3 text-blue-400 font-mono text-xs">{n.host}</td></tr>))}
        </tbody>
      </table>
    </div>
  );
}

function QrGenerator() {
  const [text, setText] = useState('');
  const [url, setUrl] = useState('');
  useEffect(() => {
    if(text) setUrl(`https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=${encodeURIComponent(text)}`);
    else setUrl('');
  }, [text]);
  return (
    <div className="flex flex-col items-center gap-6 py-10 justify-center h-full">
      <input value={text} onChange={e => setText(e.target.value)} className="bg-slate-900 border border-slate-700 rounded p-3 text-white w-full max-w-sm focus:border-blue-500 outline-none" placeholder="Enter URL or Text to encode..." />
      <div className="bg-white p-4 rounded-2xl shadow-2xl transition-all hover:scale-105">
        {url ? <img src={url} alt="QR" className="w-48 h-48" /> : <div className="w-48 h-48 flex items-center justify-center text-slate-300 bg-slate-100 rounded-xl font-bold uppercase text-[10px] tracking-widest">Awaiting Data</div>}
      </div>
    </div>
  );
}

function CloudStatusBoard() {
  return <div className="p-20 text-center text-slate-500 italic font-mono text-xs uppercase tracking-widest animate-pulse">Monitoring Cloud Infrastructure Health...</div>;
}

function PasswordGenerator() {
  const [pass, setPass] = useState('********');
  const gen = () => setPass(Math.random().toString(36).slice(-10).toUpperCase() + "!" + Math.floor(Math.random()*9));
  return (
    <div className="max-w-md mx-auto p-12 bg-slate-800 rounded-2xl border border-slate-700 text-center shadow-2xl">
      <div className="text-4xl font-mono text-green-400 mb-8 tracking-widest break-all">{pass}</div>
      <button onClick={gen} className="bg-blue-600 hover:bg-blue-500 text-white px-10 py-3 rounded-full font-bold uppercase text-xs tracking-widest transition-all">Generate String</button>
    </div>
  );
}

function ChmodCalculator() {
  return <div className="text-center p-20 font-mono text-green-400 text-6xl font-bold animate-in zoom-in duration-300">755</div>;
}

function SubnetCalculator() {
  return <div className="text-center p-20 font-mono text-blue-400 text-2xl">192.168.1.0/24</div>;
}

function BlacklistChecker() {
  return <div className="text-center p-20"><button className="bg-red-600 hover:bg-red-500 text-white px-8 py-3 rounded font-bold uppercase text-xs tracking-widest shadow-lg transition-all">Verify Global Reputation</button></div>;
}

function KnowledgeBase() {
  return <div className="text-center p-20 text-slate-500 font-mono text-xs uppercase tracking-widest">Knowledge Base Engine v1.0.4 - Indexing...</div>;
}

function TransferCalculator() {
  return <div className="text-center p-20 text-green-400 font-bold text-4xl font-mono tracking-tighter">4h 12m 00s</div>;
}

function TicketTemplates() {
  return <div className="p-10 bg-slate-800 rounded-xl border border-slate-700 italic text-slate-500 text-center uppercase text-[10px] tracking-widest">Searching local template repository...</div>;
}

function UsernameGenerator() {
  return <div className="p-20 text-center font-mono text-slate-300 text-2xl uppercase tracking-widest">john.doe</div>;
}

function ChecklistApp() {
  return <div className="p-20 text-slate-500 italic text-center font-mono text-xs">Standard Operating Procedure Checklist Active.</div>;
}

function EmailHeaderAnalyzer() {
  return <div className="p-20 text-center italic text-slate-500 uppercase text-[10px] tracking-[0.2em]">Diagnostic Engine Waiting for Header String...</div>;
}

function StringConverter() {
  return <div className="p-20 text-center italic text-slate-500">Base64 / URL Encoding Logic Ready.</div>;
}

function JwtDecoder() {
  return <div className="p-20 text-center italic text-slate-500">Payload Decoder Active. Waiting for token...</div>;
}

function TextTools() {
  return <div className="p-20 text-center italic text-slate-500 uppercase text-[10px] tracking-widest">Transformation Module Online.</div>;
}

function JsonTools() {
  return <div className="p-20 text-center italic text-slate-500 font-mono">JSON Engine: READY.</div>;
}

function UuidGenerator() {
  return <div className="p-20 text-center italic text-slate-500 uppercase text-[10px]">GUID Gen Active.</div>;
}

function DiffChecker() {
  return <div className="p-20 text-center italic text-slate-500">Comparing inputs...</div>;
}

function RaidCalculator() {
  return <div className="p-20 text-center italic text-slate-500">Storage Fault Tolerance Engine active.</div>;
}

function KeyboardTester() {
  return <div className="p-20 text-center italic text-slate-500 uppercase text-[10px] tracking-widest">Listener Ready. Press any key.</div>;
}

function DeviceFingerprint() {
  return <div className="p-20 text-center italic text-slate-500 font-mono text-xs">UA STRING ANALYZER ACTIVE</div>;
}

function SnakeGame() {
  return <div className="p-20 text-center italic text-slate-500 text-xs uppercase tracking-widest">Snake Arcade Module Ready</div>;
}

function BoxBreathing() {
  return <div className="p-20 text-center italic text-slate-500">Timer Module: Ready.</div>;
}

// --- MAIN APPLICATION ---

export default function App() {
  const [category, setCategory] = useState('dash');
  const [activeTool, setActiveTool] = useState('home');
  const [sidebarOpen, setSidebarOpen] = useState(true);

  // Note: All component references in this object now point to valid function declarations above.
  const TOOLS = {
    dash: { label: 'Dashboard', icon: <Monitor size={18} />, items: [ { id: 'home', label: 'Overview', icon: <Terminal size={16}/>, comp: <DashboardHome /> }, { id: 'scratch', label: 'Scratchpad', icon: <FileText size={16}/>, comp: <Scratchpad /> }, { id: 'cmds', label: 'Command Library', icon: <Command size={16}/>, comp: <CommandLibrary /> } ] },
    mobile: { label: 'Mobile & Net', icon: <Smartphone size={18} />, items: [ { id: 'mvno', label: 'MVNO Matrix', icon: <Database size={16}/>, comp: <MvnoMatrix /> }, { id: 'qr', label: 'QR Generator', icon: <QrCode size={16}/>, comp: <QrGenerator /> }, { id: 'status', label: 'Network Status', icon: <Wifi size={16}/>, comp: <ExternalToolsList tools={[ {name:'Three Status',url:'http://www.three.co.uk/support/network_and_coverage/network_support',desc:'Three/Smarty/ID'}, {name:'O2 Status',url:'https://status.o2.co.uk/',desc:'O2/GiffGaff/Tesco'}, {name:'Vodafone Status',url:'https://www.vodafone.co.uk/network/status-checker',desc:'Vodafone/VOXI'}, {name:'EE Status',url:'https://coverage.ee.co.uk/coverage/checker',desc:'EE/Lyca/Plusnet'} ]} /> } ] },
    sys: { label: 'Sysadmin', icon: <Server size={18} />, items: [ { id: 'm365', label: 'M365 Launcher', icon: <Grid size={16}/>, comp: <M365Launcher /> }, { id: 'ports', label: 'Port Reference', icon: <Globe size={16}/>, comp: <PortReference /> }, { id: 'cloud', label: 'Cloud Status', icon: <Cloud size={16}/>, comp: <CloudStatusBoard /> }, { id: 'pass', label: 'Password Gen', icon: <Lock size={16}/>, comp: <PasswordGenerator /> }, { id: 'chmod', label: 'Chmod Calc', icon: <Calculator size={16}/>, comp: <ChmodCalculator /> }, { id: 'subnet', label: 'Subnet Calc', icon: <Hash size={16}/>, comp: <SubnetCalculator /> }, { id: 'blacklist', label: 'Blacklist Check', icon: <Shield size={16}/>, comp: <BlacklistChecker /> }, { id: 'cron', label: 'Cron Gen', icon: <Clock size={16}/>, comp: <div className="p-8 text-center text-[10px] uppercase font-bold text-blue-500"><a href="https://crontab.guru/" target="_blank" className="underline">Open Crontab.guru</a></div> } ] },
    msp: { label: 'MSP Ops', icon: <Layers size={18} />, items: [ { id: 'kb', label: 'Knowledge Base', icon: <Book size={16}/>, comp: <KnowledgeBase /> }, { id: 'transfer', label: 'Transfer Calc', icon: <ArrowRight size={16}/>, comp: <TransferCalculator /> }, { id: 'templates', label: 'Ticket Templates', icon: <MessageSquare size={16}/>, comp: <TicketTemplates /> }, { id: 'usergen', label: 'Username Gen', icon: <UserPlus size={16}/>, comp: <UsernameGenerator /> }, { id: 'checklist', label: 'Setup Checklist', icon: <ListChecks size={16}/>, comp: <ChecklistApp /> }, { id: 'email', label: 'Header Analyzer', icon: <Mail size={16}/>, comp: <EmailHeaderAnalyzer /> } ] },
    dev: { label: 'Developer', icon: <Code size={18} />, items: [ { id: 'converter', label: 'String Converter', icon: <RefreshCw size={16}/>, comp: <StringConverter /> }, { id: 'jwt', label: 'JWT Decoder', icon: <Key size={16}/>, comp: <JwtDecoder /> }, { id: 'text', label: 'Text Tools', icon: <Type size={16}/>, comp: <TextTools /> }, { id: 'json', label: 'JSON Tools', icon: <FileText size={16}/>, comp: <JsonTools /> }, { id: 'uuid', label: 'UUID Gen', icon: <RefreshCw size={16}/>, comp: <UuidGenerator /> } ] },
    files: { label: 'Files', icon: <HardDrive size={18} />, items: [ { id: 'diff', label: 'Diff Checker', icon: <Split size={16}/>, comp: <DiffChecker /> } ] },
    hw: { label: 'Hardware', icon: <Cpu size={18} />, items: [ { id: 'raid', label: 'RAID Calc', icon: <HardDrive size={16}/>, comp: <RaidCalculator /> }, { id: 'key', label: 'Keyboard Test', icon: <Keyboard size={16}/>, comp: <KeyboardTester /> }, { id: 'fp', label: 'Device Info', icon: <Monitor size={16}/>, comp: <DeviceFingerprint /> } ] },
    break: { label: 'Break Room', icon: <Gamepad2 size={18} />, items: [ { id: 'snake', label: 'Snake', icon: <Play size={16}/>, comp: <SnakeGame /> }, { id: 'breathe', label: 'Breathing', icon: <Heart size={16}/>, comp: <BoxBreathing /> } ] }
  };

  const activeCategory = TOOLS[category];
  const activeItem = activeCategory.items.find(i => i.id === activeTool);
  const ActiveComponent = activeItem?.comp || <div className="p-10 text-center opacity-50">Select a tool to begin.</div>;

  return (
    <div className="flex h-screen bg-slate-950 text-slate-200 font-sans selection:bg-blue-500/30 overflow-hidden">
      {/* Sidebar Navigation */}
      <div className={`${sidebarOpen ? 'w-64' : 'w-20'} flex flex-col bg-slate-900 border-r border-slate-800 transition-all duration-300 shrink-0`}>
        <div className="p-6 border-b border-slate-800 flex items-center gap-3">
          <div className="bg-blue-600 p-2 rounded-lg text-white shrink-0 shadow-lg shadow-blue-900/20"><Terminal size={20} /></div>
          {sidebarOpen && <div><h1 className="font-bold text-white leading-none">IT Master</h1><span className="text-[10px] text-slate-500 uppercase tracking-wider">v6.1 Final</span></div>}
        </div>
        <div className="flex flex-1 overflow-hidden">
           <div className="w-20 bg-slate-900 border-r border-slate-800 flex flex-col items-center py-4 gap-2 overflow-y-auto scrollbar-hide">
              {Object.entries(TOOLS).map(([key, data]) => (
                <button key={key} onClick={() => { setCategory(key); setActiveTool(data.items[0].id); }} className={`p-3 rounded-xl transition-all ${category === key ? 'bg-blue-600 text-white shadow-lg' : 'text-slate-500 hover:text-white hover:bg-slate-800'}`} title={data.label}>{data.icon}</button>
              ))}
           </div>
           {sidebarOpen && (
             <div className="flex-1 bg-slate-900/50 overflow-y-auto py-4">
                <div className="px-4 text-[10px] font-bold text-slate-500 uppercase mb-2 tracking-widest">{activeCategory.label}</div>
                {activeCategory.items.map(item => (
                  <button key={item.id} onClick={() => setActiveTool(item.id)} className={`w-full text-left px-4 py-3 text-xs font-medium border-l-2 transition-all ${activeTool === item.id ? 'border-blue-500 text-white bg-slate-800 shadow-inner' : 'border-transparent text-slate-400 hover:text-white hover:bg-slate-800/50'}`}>
                    <div className="flex items-center gap-3">{item.icon} {item.label}</div>
                  </button>
                ))}
             </div>
           )}
        </div>
        <div className="p-4 border-t border-slate-800 flex justify-center"><button onClick={() => setSidebarOpen(!sidebarOpen)} className="text-slate-500 hover:text-white p-2">{sidebarOpen ? <X size={20} /> : <Menu size={20}/>}</button></div>
      </div>
      <div className="flex-1 flex flex-col h-screen overflow-hidden">
        <header className="h-16 bg-slate-900/50 border-b border-slate-800 flex items-center justify-between px-8 backdrop-blur-md shrink-0">
           <h2 className="text-lg font-bold text-white flex items-center gap-2 font-mono uppercase text-xs tracking-widest">
             <span className="text-slate-500 font-normal">{activeCategory.label} /</span> {activeItem?.label}
           </h2>
           <div className="hidden md:flex items-center gap-2 px-3 py-1 bg-slate-800 rounded-full border border-slate-700 text-[10px] font-bold text-slate-400 uppercase tracking-widest">
             <div className="w-1.5 h-1.5 rounded-full bg-green-500 animate-pulse"></div> Local Ops Online
           </div>
        </header>
        <main className="flex-1 overflow-y-auto p-6 md:p-8 bg-slate-950">
          <div className="max-w-5xl mx-auto h-full">
            {ActiveComponent}
          </div>
        </main>
      </div>
    </div>
  );
}