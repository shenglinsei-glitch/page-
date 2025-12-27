<!DOCTYPE html>
<html lang="ja"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>設定</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=M+PLUS+Rounded+1c:wght@300;400;500;700;800&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "selected": "#53BEE8",
                        "selected-light": "#B2E3F4",
                        "text-main": "#5E5E5E",    // Content text
                        "text-sub": "#C6CBD4",     // Title / Sub text
                        "icon-col": "#53BEE8",     // Icon color
                        "icon-shadow": "#E5EBF2",  // Icon shadow color
                        "background-light": "#FFFFFF", // Forced white as requested
                        "background-dark": "#101622",
                        "danger": "#FF5B5B",
                    },
                    fontFamily: {
                        "display": ["M PLUS Rounded 1c", "sans-serif"]
                    },
                    boxShadow: {
                        'icon': '0 2px 4px var(--icon-shadow)',
                        'soft': '0 4px 20px -2px rgba(229, 235, 242, 0.6)', 
                        'glow': '0 8px 24px -4px rgba(83, 190, 232, 0.45)', 
                        'setting-card': '0 2px 12px rgba(229, 235, 242, 0.5)',
                        'toggle-knob': '0 1px 3px rgba(0,0,0,0.15)',
                    },
                    borderRadius: {"DEFAULT": "0.25rem", "lg": "0.5rem", "xl": "0.75rem", "2xl": "1rem", "3xl": "1.5rem", "full": "9999px"},
                },
            },
        }
    </script>
<style>
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
        .icon-shadow-filter {
            filter: drop-shadow(1px 1px 0px #E5EBF2); 
            text-shadow: 1px 1px 0px #E5EBF2;
        }
        body {
            min-height: max(884px, 100dvh);
        }
    </style>
<style>
    body {
      min-height: max(884px, 100dvh);
    }
  </style>
  </head>
<body class="bg-background-light font-display antialiased text-slate-900 relative">
<div class="relative flex h-full min-h-screen w-full flex-col max-w-md mx-auto overflow-hidden bg-background-light">
<header class="sticky top-0 z-20 flex items-center justify-between px-4 py-4 bg-white/90 backdrop-blur-md relative">
<button class="flex items-center justify-center text-icon-col transition-opacity hover:opacity-80 -ml-2 p-2 active:scale-95 duration-200 rounded-full z-10">
<span class="material-symbols-outlined text-[28px] icon-shadow-filter">chevron_left</span>
</button>
<h1 class="absolute left-1/2 top-1/2 transform -translate-x-1/2 -translate-y-1/2 text-[17px] font-bold text-text-sub text-center pointer-events-none">設定</h1>
</header>
<main class="flex-1 overflow-y-auto no-scrollbar px-5 pb-10 pt-2">
<div class="flex flex-col gap-6">
<div class="flex flex-col gap-2">
<h2 class="px-1 text-xs font-bold text-text-sub">外観 / 表示</h2>
<div class="flex flex-col bg-white rounded-2xl shadow-setting-card border border-slate-50 overflow-hidden">
<div class="flex items-center justify-between p-4 border-b border-slate-50">
<div class="flex items-center gap-3">
<span class="material-symbols-outlined text-[24px] text-icon-col icon-shadow-filter">dark_mode</span>
<span class="text-[15px] font-medium text-text-main">深色模式</span>
</div>
<label class="relative inline-flex items-center cursor-pointer p-3 -mr-3 select-none">
<input class="sr-only peer" id="dark-mode-toggle" type="checkbox"/>
<div class="w-[3.25rem] h-7 bg-slate-200 peer-focus:outline-none rounded-full peer peer-checked:bg-icon-col transition-colors duration-300"></div>
<div class="absolute left-[14px] top-[14px] bg-white w-6 h-6 rounded-full shadow-toggle-knob transition-all duration-300 peer-checked:translate-x-6"></div>
</label>
</div>
<div class="flex items-center justify-between p-4 active:bg-slate-50 transition-colors cursor-pointer">
<div class="flex items-center gap-3">
<span class="material-symbols-outlined text-[24px] text-icon-col icon-shadow-filter">language</span>
<span class="text-[15px] font-medium text-text-main">语言显示</span>
</div>
<div class="flex items-center gap-1">
<span class="text-xs text-text-sub">日本語</span>
<span class="material-symbols-outlined text-text-sub text-[20px]">chevron_right</span>
</div>
</div>
</div>
</div>
<div class="flex flex-col gap-2">
<h2 class="px-1 text-xs font-bold text-text-sub">発音</h2>
<div class="flex flex-col bg-white rounded-2xl shadow-setting-card border border-slate-50 overflow-hidden">
<div class="flex items-center justify-between p-4 border-b border-slate-50">
<div class="flex items-center gap-3">
<span class="material-symbols-outlined text-[24px] text-icon-col icon-shadow-filter">smart_display</span>
<span class="text-[15px] font-medium text-text-main">自動再生</span>
</div>
<label class="relative inline-flex items-center cursor-pointer p-3 -mr-3 select-none">
<input checked="" class="sr-only peer" id="autoplay-toggle" type="checkbox"/>
<div class="w-[3.25rem] h-7 bg-slate-200 peer-focus:outline-none rounded-full peer peer-checked:bg-icon-col transition-colors duration-300"></div>
<div class="absolute left-[14px] top-[14px] bg-white w-6 h-6 rounded-full shadow-toggle-knob transition-all duration-300 peer-checked:translate-x-6"></div>
</label>
</div>
<div class="flex items-center justify-between p-4 active:bg-slate-50 transition-colors cursor-pointer">
<div class="flex items-center gap-3">
<span class="material-symbols-outlined text-[24px] text-icon-col icon-shadow-filter">record_voice_over</span>
<span class="text-[15px] font-medium text-text-main">デフォルト言語</span>
</div>
<div class="flex items-center gap-1">
<span class="text-xs text-text-sub">English</span>
<span class="material-symbols-outlined text-text-sub text-[20px]">chevron_right</span>
</div>
</div>
</div>
</div>
<div class="flex flex-col gap-2">
<h2 class="px-1 text-xs font-bold text-text-sub">データ</h2>
<div class="flex flex-col bg-white rounded-2xl shadow-setting-card border border-slate-50 overflow-hidden">
<div class="flex items-center justify-between p-4 border-b border-slate-50 active:bg-slate-50 transition-colors cursor-pointer">
<div class="flex items-center gap-3">
<span class="material-symbols-outlined text-[24px] text-icon-col icon-shadow-filter">download</span>
<span class="text-[15px] font-medium text-text-main">インポート</span>
</div>
<span class="material-symbols-outlined text-text-sub text-[20px]">chevron_right</span>
</div>
<div class="flex items-center justify-between p-4 border-b border-slate-50 active:bg-slate-50 transition-colors cursor-pointer">
<div class="flex items-center gap-3">
<span class="material-symbols-outlined text-[24px] text-icon-col icon-shadow-filter">upload</span>
<span class="text-[15px] font-medium text-text-main">エクスポート</span>
</div>
<span class="material-symbols-outlined text-text-sub text-[20px]">chevron_right</span>
</div>
<div class="flex items-center justify-between p-4 bg-slate-50/50 cursor-not-allowed">
<div class="flex items-center gap-3 opacity-40 grayscale">
<span class="material-symbols-outlined text-[24px] text-icon-col icon-shadow-filter">cloud_upload</span>
<span class="text-[15px] font-medium text-text-main">バックアップ</span>
</div>
</div>
</div>
</div>
<div class="flex flex-col gap-2">
<h2 class="px-1 text-xs font-bold text-text-sub">その他</h2>
<div class="flex flex-col bg-white rounded-2xl shadow-setting-card border border-slate-50 overflow-hidden">
<div class="flex items-center justify-between p-4 border-b border-slate-50 active:bg-slate-50 transition-colors cursor-pointer">
<div class="flex items-center gap-3">
<span class="material-symbols-outlined text-[24px] text-icon-col icon-shadow-filter">menu_book</span>
<span class="text-[15px] font-medium text-text-main">使用説明</span>
</div>
<span class="material-symbols-outlined text-text-sub text-[20px]">chevron_right</span>
</div>
<div class="flex items-center justify-between p-4 active:bg-slate-50 transition-colors cursor-pointer">
<div class="flex items-center gap-3">
<span class="material-symbols-outlined text-[24px] text-icon-col icon-shadow-filter">info</span>
<span class="text-[15px] font-medium text-text-main">について</span>
</div>
<span class="material-symbols-outlined text-text-sub text-[20px]">chevron_right</span>
</div>
</div>
</div>
<div class="h-8"></div>
<div class="text-center pb-8">
<p class="text-[10px] text-text-sub font-medium">Version 1.0.2 (Build 45)</p>
</div>
</div>
</main>
</div>

</body></html>
