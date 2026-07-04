<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1,user-scalable=no"/>
<meta name="theme-color" content="#052e16"/>
<meta name="mobile-web-app-capable" content="yes"/>
<meta name="apple-mobile-web-app-capable" content="yes"/>
<meta name="apple-mobile-web-app-title" content="RR Farm"/>
<title>RR Farm Manager</title>
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Ctext y='20' font-size='22'%3E%F0%9F%8C%B1%3C/text%3E%3C/svg%3E"/>
<style>
*,::before,::after{box-sizing:border-box;border-width:0;border-style:solid;border-color:#e7e5e4}
html{line-height:1.5;-webkit-text-size-adjust:100%;font-family:ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,'Helvetica Neue',Arial,'Noto Sans',sans-serif}
body{margin:0;line-height:inherit}
h1,h2,h3,h4,h5,h6{font-size:inherit;font-weight:inherit}
a{color:inherit;text-decoration:inherit}
button,input,optgroup,select,textarea{font-family:inherit;font-size:100%;font-weight:inherit;line-height:inherit;color:inherit;margin:0;padding:0}
button{cursor:pointer;background-color:transparent;background-image:none}
:-moz-focusring{outline:auto}
:-moz-ui-invalid{box-shadow:none}
progress{vertical-align:baseline}
::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}
[type='search']{-webkit-appearance:textfield;outline-offset:-2px}
::-webkit-search-decoration{-webkit-appearance:none}
::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}
summary{display:list-item}
blockquote,dl,figure,h1,h2,h3,h4,h5,h6,hr,p,pre{margin:0}
fieldset{margin:0;padding:0}
legend{padding:0}
ol,ul,menu{list-style:none;margin:0;padding:0}
textarea{resize:vertical}
input::placeholder,textarea::placeholder{opacity:1;color:#a8a29e}
button,[role='button']{cursor:pointer}
img,svg,video,canvas,audio,iframe,embed,object{display:block;vertical-align:middle}
img,video{max-width:100%;height:auto}
[hidden]{display:none}
.flex{display:flex}
.grid{display:grid}
.hidden{display:none}
.block{display:block}
.inline{display:inline}
.fixed{position:fixed}
.absolute{position:absolute}
.sticky{position:sticky;top:0}
.inset-0{inset:0}
.top-0{top:0}
.bottom-4{bottom:1rem}
.right-4{right:1rem}
.left-0{left:0}
.flex-col{flex-direction:column}
.flex-wrap{flex-wrap:wrap}
.flex-row{flex-direction:row}
.flex-1{flex:1 1 0%}
.items-center{align-items:center}
.items-start{align-items:flex-start}
.justify-center{justify-content:center}
.justify-between{justify-content:space-between}
.justify-end{justify-content:flex-end}
.shrink-0{flex-shrink:0}
.grow{flex-grow:1}
.grid-cols-1{grid-template-columns:repeat(1,minmax(0,1fr))}
.grid-cols-2{grid-template-columns:repeat(2,minmax(0,1fr))}
.w-full{width:100%}
.min-h-screen{min-height:100vh}
.h-64{height:16rem}
.max-w-xs{max-width:20rem}
.max-w-md{max-width:28rem}
.max-w-lg{max-width:32rem}
.w-11{width:2.75rem}
.h-11{height:2.75rem}
.w-9{width:2.25rem}
.h-9{height:2.25rem}
.max-h-32{max-height:8rem}
.px-1{padding-left:0.25rem;padding-right:0.25rem}
.w-24{width:6rem}
.overflow-y-auto{overflow-y:auto}
.overflow-x-auto{overflow-x:auto}
.z-30{z-index:30}
.z-50{z-index:50}
.text-xs{font-size:0.75rem;line-height:1rem}
.text-sm{font-size:0.875rem;line-height:1.25rem}
.text-base{font-size:1rem;line-height:1.5rem}
.text-lg{font-size:1.125rem;line-height:1.75rem}
.text-2xl{font-size:1.5rem;line-height:2rem}
.font-medium{font-weight:500}
.font-semibold{font-weight:600}
.font-bold{font-weight:700}
.font-mono{font-family:ui-monospace,SFMono-Regular,Menlo,Monaco,Consolas,'Liberation Mono','Courier New',monospace}
.text-center{text-align:center}
.text-white{color:#fff}
.uppercase{text-transform:uppercase}
.tracking-tight{letter-spacing:-0.025em}
.tracking-wide{letter-spacing:0.025em}
.leading-none{line-height:1}
.whitespace-pre-line{white-space:pre-line}
.truncate{overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.border{border-width:1px;border-style:solid}
.border-b{border-bottom-width:1px;border-bottom-style:solid}
.border-t{border-top-width:1px;border-top-style:solid}
.border-l-4{border-left-width:4px;border-left-style:solid}
.border-dashed{border-style:dashed}
.rounded{border-radius:0.25rem}
.rounded-lg{border-radius:0.5rem}
.rounded-xl{border-radius:0.75rem}
.rounded-2xl{border-radius:1rem}
.rounded-full{border-radius:9999px}
.shadow-sm{box-shadow:0 1px 2px 0 rgb(0 0 0/0.05)}
.shadow-lg{box-shadow:0 10px 15px -3px rgb(0 0 0/0.1),0 4px 6px -4px rgb(0 0 0/0.1)}
.shadow-xl{box-shadow:0 20px 25px -5px rgb(0 0 0/0.1),0 8px 10px -6px rgb(0 0 0/0.1)}
.divide-y{}
.divide-y>*+*{border-top-width:1px;border-top-style:solid}
.space-y-1>*+*{margin-top:0.25rem}
.space-y-2>*+*{margin-top:0.5rem}
.space-y-3>*+*{margin-top:0.75rem}
.space-y-4>*+*{margin-top:1rem}
.gap-1{gap:0.25rem}
.gap-1\.5{gap:0.375rem}
.gap-2{gap:0.5rem}
.gap-3{gap:0.75rem}
.gap-4{gap:1rem}
.p-0{padding:0px}
.px-0{padding-left:0px;padding-right:0px}
.py-0{padding-top:0px;padding-bottom:0px}
.pt-0{padding-top:0px}
.pb-0{padding-bottom:0px}
.p-0\.5{padding:0.125rem}
.px-0\.5{padding-left:0.125rem;padding-right:0.125rem}
.py-0\.5{padding-top:0.125rem;padding-bottom:0.125rem}
.pt-0\.5{padding-top:0.125rem}
.pb-0\.5{padding-bottom:0.125rem}
.p-1{padding:0.25rem}
.px-1{padding-left:0.25rem;padding-right:0.25rem}
.py-1{padding-top:0.25rem;padding-bottom:0.25rem}
.pt-1{padding-top:0.25rem}
.pb-1{padding-bottom:0.25rem}
.p-1\.5{padding:0.375rem}
.px-1\.5{padding-left:0.375rem;padding-right:0.375rem}
.py-1\.5{padding-top:0.375rem;padding-bottom:0.375rem}
.pt-1\.5{padding-top:0.375rem}
.pb-1\.5{padding-bottom:0.375rem}
.p-2{padding:0.5rem}
.px-2{padding-left:0.5rem;padding-right:0.5rem}
.py-2{padding-top:0.5rem;padding-bottom:0.5rem}
.pt-2{padding-top:0.5rem}
.pb-2{padding-bottom:0.5rem}
.p-2\.5{padding:0.625rem}
.px-2\.5{padding-left:0.625rem;padding-right:0.625rem}
.py-2\.5{padding-top:0.625rem;padding-bottom:0.625rem}
.pt-2\.5{padding-top:0.625rem}
.pb-2\.5{padding-bottom:0.625rem}
.p-3{padding:0.75rem}
.px-3{padding-left:0.75rem;padding-right:0.75rem}
.py-3{padding-top:0.75rem;padding-bottom:0.75rem}
.pt-3{padding-top:0.75rem}
.pb-3{padding-bottom:0.75rem}
.p-4{padding:1rem}
.px-4{padding-left:1rem;padding-right:1rem}
.py-4{padding-top:1rem;padding-bottom:1rem}
.pt-4{padding-top:1rem}
.pb-4{padding-bottom:1rem}
.p-5{padding:1.25rem}
.px-5{padding-left:1.25rem;padding-right:1.25rem}
.py-5{padding-top:1.25rem;padding-bottom:1.25rem}
.pt-5{padding-top:1.25rem}
.pb-5{padding-bottom:1.25rem}
.p-6{padding:1.5rem}
.px-6{padding-left:1.5rem;padding-right:1.5rem}
.py-6{padding-top:1.5rem;padding-bottom:1.5rem}
.pt-6{padding-top:1.5rem}
.pb-6{padding-bottom:1.5rem}
.p-7{padding:1.75rem}
.px-7{padding-left:1.75rem;padding-right:1.75rem}
.py-7{padding-top:1.75rem;padding-bottom:1.75rem}
.pt-7{padding-top:1.75rem}
.pb-7{padding-bottom:1.75rem}
.p-8{padding:2rem}
.px-8{padding-left:2rem;padding-right:2rem}
.py-8{padding-top:2rem;padding-bottom:2rem}
.pt-8{padding-top:2rem}
.pb-8{padding-bottom:2rem}
.p-16{padding:4rem}
.px-16{padding-left:4rem;padding-right:4rem}
.py-16{padding-top:4rem;padding-bottom:4rem}
.pt-16{padding-top:4rem}
.pb-16{padding-bottom:4rem}
.m-0{margin:0px}
.mb-0{margin-bottom:0px}
.mt-0{margin-top:0px}
.ml-0{margin-left:0px}
.mr-0{margin-right:0px}
.mx-0{margin-left:0px;margin-right:0px}
.my-0{margin-top:0px;margin-bottom:0px}
.m-0\.5{margin:0.125rem}
.mb-0\.5{margin-bottom:0.125rem}
.mt-0\.5{margin-top:0.125rem}
.ml-0\.5{margin-left:0.125rem}
.mr-0\.5{margin-right:0.125rem}
.mx-0\.5{margin-left:0.125rem;margin-right:0.125rem}
.my-0\.5{margin-top:0.125rem;margin-bottom:0.125rem}
.m-1{margin:0.25rem}
.mb-1{margin-bottom:0.25rem}
.mt-1{margin-top:0.25rem}
.ml-1{margin-left:0.25rem}
.mr-1{margin-right:0.25rem}
.mx-1{margin-left:0.25rem;margin-right:0.25rem}
.my-1{margin-top:0.25rem;margin-bottom:0.25rem}
.m-1\.5{margin:0.375rem}
.mb-1\.5{margin-bottom:0.375rem}
.mt-1\.5{margin-top:0.375rem}
.ml-1\.5{margin-left:0.375rem}
.mr-1\.5{margin-right:0.375rem}
.mx-1\.5{margin-left:0.375rem;margin-right:0.375rem}
.my-1\.5{margin-top:0.375rem;margin-bottom:0.375rem}
.m-2{margin:0.5rem}
.mb-2{margin-bottom:0.5rem}
.mt-2{margin-top:0.5rem}
.ml-2{margin-left:0.5rem}
.mr-2{margin-right:0.5rem}
.mx-2{margin-left:0.5rem;margin-right:0.5rem}
.my-2{margin-top:0.5rem;margin-bottom:0.5rem}
.m-2\.5{margin:0.625rem}
.mb-2\.5{margin-bottom:0.625rem}
.mt-2\.5{margin-top:0.625rem}
.ml-2\.5{margin-left:0.625rem}
.mr-2\.5{margin-right:0.625rem}
.mx-2\.5{margin-left:0.625rem;margin-right:0.625rem}
.my-2\.5{margin-top:0.625rem;margin-bottom:0.625rem}
.m-3{margin:0.75rem}
.mb-3{margin-bottom:0.75rem}
.mt-3{margin-top:0.75rem}
.ml-3{margin-left:0.75rem}
.mr-3{margin-right:0.75rem}
.mx-3{margin-left:0.75rem;margin-right:0.75rem}
.my-3{margin-top:0.75rem;margin-bottom:0.75rem}
.m-4{margin:1rem}
.mb-4{margin-bottom:1rem}
.mt-4{margin-top:1rem}
.ml-4{margin-left:1rem}
.mr-4{margin-right:1rem}
.mx-4{margin-left:1rem;margin-right:1rem}
.my-4{margin-top:1rem;margin-bottom:1rem}
.m-5{margin:1.25rem}
.mb-5{margin-bottom:1.25rem}
.mt-5{margin-top:1.25rem}
.ml-5{margin-left:1.25rem}
.mr-5{margin-right:1.25rem}
.mx-5{margin-left:1.25rem;margin-right:1.25rem}
.my-5{margin-top:1.25rem;margin-bottom:1.25rem}
.m-6{margin:1.5rem}
.mb-6{margin-bottom:1.5rem}
.mt-6{margin-top:1.5rem}
.ml-6{margin-left:1.5rem}
.mr-6{margin-right:1.5rem}
.mx-6{margin-left:1.5rem;margin-right:1.5rem}
.my-6{margin-top:1.5rem;margin-bottom:1.5rem}
.m-7{margin:1.75rem}
.mb-7{margin-bottom:1.75rem}
.mt-7{margin-top:1.75rem}
.ml-7{margin-left:1.75rem}
.mr-7{margin-right:1.75rem}
.mx-7{margin-left:1.75rem;margin-right:1.75rem}
.my-7{margin-top:1.75rem;margin-bottom:1.75rem}
.m-8{margin:2rem}
.mb-8{margin-bottom:2rem}
.mt-8{margin-top:2rem}
.ml-8{margin-left:2rem}
.mr-8{margin-right:2rem}
.mx-8{margin-left:2rem;margin-right:2rem}
.my-8{margin-top:2rem;margin-bottom:2rem}
.bg-stone-50{background-color:#fafaf9}
.text-stone-50{color:#fafaf9}
.border-stone-50{border-color:#fafaf9}
.border-l-stone-50{border-left-color:#fafaf9}
.divide-stone-50{--tw-divide-color:#fafaf9}
.divide-stone-50>*+*{border-color:#fafaf9}
.bg-stone-100{background-color:#f5f5f4}
.text-stone-100{color:#f5f5f4}
.border-stone-100{border-color:#f5f5f4}
.border-l-stone-100{border-left-color:#f5f5f4}
.divide-stone-100{--tw-divide-color:#f5f5f4}
.divide-stone-100>*+*{border-color:#f5f5f4}
.bg-stone-200{background-color:#e7e5e4}
.text-stone-200{color:#e7e5e4}
.border-stone-200{border-color:#e7e5e4}
.border-l-stone-200{border-left-color:#e7e5e4}
.divide-stone-200{--tw-divide-color:#e7e5e4}
.divide-stone-200>*+*{border-color:#e7e5e4}
.bg-stone-300{background-color:#d6d3d1}
.text-stone-300{color:#d6d3d1}
.border-stone-300{border-color:#d6d3d1}
.border-l-stone-300{border-left-color:#d6d3d1}
.divide-stone-300{--tw-divide-color:#d6d3d1}
.divide-stone-300>*+*{border-color:#d6d3d1}
.bg-stone-400{background-color:#a8a29e}
.text-stone-400{color:#a8a29e}
.border-stone-400{border-color:#a8a29e}
.border-l-stone-400{border-left-color:#a8a29e}
.divide-stone-400{--tw-divide-color:#a8a29e}
.divide-stone-400>*+*{border-color:#a8a29e}
.bg-stone-500{background-color:#78716c}
.text-stone-500{color:#78716c}
.border-stone-500{border-color:#78716c}
.border-l-stone-500{border-left-color:#78716c}
.divide-stone-500{--tw-divide-color:#78716c}
.divide-stone-500>*+*{border-color:#78716c}
.bg-stone-600{background-color:#57534e}
.text-stone-600{color:#57534e}
.border-stone-600{border-color:#57534e}
.border-l-stone-600{border-left-color:#57534e}
.divide-stone-600{--tw-divide-color:#57534e}
.divide-stone-600>*+*{border-color:#57534e}
.bg-stone-700{background-color:#44403c}
.text-stone-700{color:#44403c}
.border-stone-700{border-color:#44403c}
.border-l-stone-700{border-left-color:#44403c}
.divide-stone-700{--tw-divide-color:#44403c}
.divide-stone-700>*+*{border-color:#44403c}
.bg-stone-800{background-color:#292524}
.text-stone-800{color:#292524}
.border-stone-800{border-color:#292524}
.border-l-stone-800{border-left-color:#292524}
.divide-stone-800{--tw-divide-color:#292524}
.divide-stone-800>*+*{border-color:#292524}
.bg-stone-900{background-color:#1c1917}
.text-stone-900{color:#1c1917}
.border-stone-900{border-color:#1c1917}
.border-l-stone-900{border-left-color:#1c1917}
.divide-stone-900{--tw-divide-color:#1c1917}
.divide-stone-900>*+*{border-color:#1c1917}
.bg-stone-950{background-color:#0c0a09}
.text-stone-950{color:#0c0a09}
.border-stone-950{border-color:#0c0a09}
.border-l-stone-950{border-left-color:#0c0a09}
.divide-stone-950{--tw-divide-color:#0c0a09}
.divide-stone-950>*+*{border-color:#0c0a09}
.bg-green-50{background-color:#f0fdf4}
.text-green-50{color:#f0fdf4}
.border-green-50{border-color:#f0fdf4}
.border-l-green-50{border-left-color:#f0fdf4}
.divide-green-50{--tw-divide-color:#f0fdf4}
.divide-green-50>*+*{border-color:#f0fdf4}
.bg-green-100{background-color:#dcfce7}
.text-green-100{color:#dcfce7}
.border-green-100{border-color:#dcfce7}
.border-l-green-100{border-left-color:#dcfce7}
.divide-green-100{--tw-divide-color:#dcfce7}
.divide-green-100>*+*{border-color:#dcfce7}
.bg-green-200{background-color:#bbf7d0}
.text-green-200{color:#bbf7d0}
.border-green-200{border-color:#bbf7d0}
.border-l-green-200{border-left-color:#bbf7d0}
.divide-green-200{--tw-divide-color:#bbf7d0}
.divide-green-200>*+*{border-color:#bbf7d0}
.bg-green-300{background-color:#86efac}
.text-green-300{color:#86efac}
.border-green-300{border-color:#86efac}
.border-l-green-300{border-left-color:#86efac}
.divide-green-300{--tw-divide-color:#86efac}
.divide-green-300>*+*{border-color:#86efac}
.bg-green-400{background-color:#4ade80}
.text-green-400{color:#4ade80}
.border-green-400{border-color:#4ade80}
.border-l-green-400{border-left-color:#4ade80}
.divide-green-400{--tw-divide-color:#4ade80}
.divide-green-400>*+*{border-color:#4ade80}
.bg-green-600{background-color:#16a34a}
.text-green-600{color:#16a34a}
.border-green-600{border-color:#16a34a}
.border-l-green-600{border-left-color:#16a34a}
.divide-green-600{--tw-divide-color:#16a34a}
.divide-green-600>*+*{border-color:#16a34a}
.bg-green-700{background-color:#15803d}
.text-green-700{color:#15803d}
.border-green-700{border-color:#15803d}
.border-l-green-700{border-left-color:#15803d}
.divide-green-700{--tw-divide-color:#15803d}
.divide-green-700>*+*{border-color:#15803d}
.bg-green-800{background-color:#166534}
.text-green-800{color:#166534}
.border-green-800{border-color:#166534}
.border-l-green-800{border-left-color:#166534}
.divide-green-800{--tw-divide-color:#166534}
.divide-green-800>*+*{border-color:#166534}
.bg-green-900{background-color:#14532d}
.text-green-900{color:#14532d}
.border-green-900{border-color:#14532d}
.border-l-green-900{border-left-color:#14532d}
.divide-green-900{--tw-divide-color:#14532d}
.divide-green-900>*+*{border-color:#14532d}
.bg-green-950{background-color:#052e16}
.text-green-950{color:#052e16}
.border-green-950{border-color:#052e16}
.border-l-green-950{border-left-color:#052e16}
.divide-green-950{--tw-divide-color:#052e16}
.divide-green-950>*+*{border-color:#052e16}
.bg-blue-50{background-color:#eff6ff}
.text-blue-50{color:#eff6ff}
.border-blue-50{border-color:#eff6ff}
.border-l-blue-50{border-left-color:#eff6ff}
.divide-blue-50{--tw-divide-color:#eff6ff}
.divide-blue-50>*+*{border-color:#eff6ff}
.bg-blue-100{background-color:#dbeafe}
.text-blue-100{color:#dbeafe}
.border-blue-100{border-color:#dbeafe}
.border-l-blue-100{border-left-color:#dbeafe}
.divide-blue-100{--tw-divide-color:#dbeafe}
.divide-blue-100>*+*{border-color:#dbeafe}
.bg-blue-200{background-color:#bfdbfe}
.text-blue-200{color:#bfdbfe}
.border-blue-200{border-color:#bfdbfe}
.border-l-blue-200{border-left-color:#bfdbfe}
.divide-blue-200{--tw-divide-color:#bfdbfe}
.divide-blue-200>*+*{border-color:#bfdbfe}
.bg-blue-600{background-color:#2563eb}
.text-blue-600{color:#2563eb}
.border-blue-600{border-color:#2563eb}
.border-l-blue-600{border-left-color:#2563eb}
.divide-blue-600{--tw-divide-color:#2563eb}
.divide-blue-600>*+*{border-color:#2563eb}
.bg-blue-700{background-color:#1d4ed8}
.text-blue-700{color:#1d4ed8}
.border-blue-700{border-color:#1d4ed8}
.border-l-blue-700{border-left-color:#1d4ed8}
.divide-blue-700{--tw-divide-color:#1d4ed8}
.divide-blue-700>*+*{border-color:#1d4ed8}
.bg-red-50{background-color:#fef2f2}
.text-red-50{color:#fef2f2}
.border-red-50{border-color:#fef2f2}
.border-l-red-50{border-left-color:#fef2f2}
.divide-red-50{--tw-divide-color:#fef2f2}
.divide-red-50>*+*{border-color:#fef2f2}
.bg-red-100{background-color:#fee2e2}
.text-red-100{color:#fee2e2}
.border-red-100{border-color:#fee2e2}
.border-l-red-100{border-left-color:#fee2e2}
.divide-red-100{--tw-divide-color:#fee2e2}
.divide-red-100>*+*{border-color:#fee2e2}
.bg-red-200{background-color:#fecaca}
.text-red-200{color:#fecaca}
.border-red-200{border-color:#fecaca}
.border-l-red-200{border-left-color:#fecaca}
.divide-red-200{--tw-divide-color:#fecaca}
.divide-red-200>*+*{border-color:#fecaca}
.bg-red-600{background-color:#dc2626}
.text-red-600{color:#dc2626}
.border-red-600{border-color:#dc2626}
.border-l-red-600{border-left-color:#dc2626}
.divide-red-600{--tw-divide-color:#dc2626}
.divide-red-600>*+*{border-color:#dc2626}
.bg-red-700{background-color:#b91c1c}
.text-red-700{color:#b91c1c}
.border-red-700{border-color:#b91c1c}
.border-l-red-700{border-left-color:#b91c1c}
.divide-red-700{--tw-divide-color:#b91c1c}
.divide-red-700>*+*{border-color:#b91c1c}
.bg-amber-50{background-color:#fffbeb}
.text-amber-50{color:#fffbeb}
.border-amber-50{border-color:#fffbeb}
.border-l-amber-50{border-left-color:#fffbeb}
.divide-amber-50{--tw-divide-color:#fffbeb}
.divide-amber-50>*+*{border-color:#fffbeb}
.bg-amber-100{background-color:#fef3c7}
.text-amber-100{color:#fef3c7}
.border-amber-100{border-color:#fef3c7}
.border-l-amber-100{border-left-color:#fef3c7}
.divide-amber-100{--tw-divide-color:#fef3c7}
.divide-amber-100>*+*{border-color:#fef3c7}
.bg-amber-200{background-color:#fde68a}
.text-amber-200{color:#fde68a}
.border-amber-200{border-color:#fde68a}
.border-l-amber-200{border-left-color:#fde68a}
.divide-amber-200{--tw-divide-color:#fde68a}
.divide-amber-200>*+*{border-color:#fde68a}
.bg-amber-400{background-color:#fbbf24}
.text-amber-400{color:#fbbf24}
.border-amber-400{border-color:#fbbf24}
.border-l-amber-400{border-left-color:#fbbf24}
.divide-amber-400{--tw-divide-color:#fbbf24}
.divide-amber-400>*+*{border-color:#fbbf24}
.bg-amber-600{background-color:#d97706}
.text-amber-600{color:#d97706}
.border-amber-600{border-color:#d97706}
.border-l-amber-600{border-left-color:#d97706}
.divide-amber-600{--tw-divide-color:#d97706}
.divide-amber-600>*+*{border-color:#d97706}
.bg-amber-700{background-color:#b45309}
.text-amber-700{color:#b45309}
.border-amber-700{border-color:#b45309}
.border-l-amber-700{border-left-color:#b45309}
.divide-amber-700{--tw-divide-color:#b45309}
.divide-amber-700>*+*{border-color:#b45309}
.bg-amber-800{background-color:#92400e}
.text-amber-800{color:#92400e}
.border-amber-800{border-color:#92400e}
.border-l-amber-800{border-left-color:#92400e}
.divide-amber-800{--tw-divide-color:#92400e}
.divide-amber-800>*+*{border-color:#92400e}
.bg-white{background-color:#ffffff}
.text-white{color:#ffffff}
.border-white{border-color:#ffffff}
.border-l-white{border-left-color:#ffffff}
.divide-white{--tw-divide-color:#ffffff}
.divide-white>*+*{border-color:#ffffff}
.hover\:bg-stone-50{background-color:#fafaf9}
.hover\:text-stone-50{color:#fafaf9}
.hover\:bg-stone-100{background-color:#f5f5f4}
.hover\:text-stone-100{color:#f5f5f4}
.hover\:bg-stone-200{background-color:#e7e5e4}
.hover\:text-stone-200{color:#e7e5e4}
.hover\:bg-stone-300{background-color:#d6d3d1}
.hover\:text-stone-300{color:#d6d3d1}
.hover\:bg-stone-400{background-color:#a8a29e}
.hover\:text-stone-400{color:#a8a29e}
.hover\:bg-stone-500{background-color:#78716c}
.hover\:text-stone-500{color:#78716c}
.hover\:bg-stone-600{background-color:#57534e}
.hover\:text-stone-600{color:#57534e}
.hover\:bg-stone-700{background-color:#44403c}
.hover\:text-stone-700{color:#44403c}
.hover\:bg-stone-800{background-color:#292524}
.hover\:text-stone-800{color:#292524}
.hover\:bg-stone-900{background-color:#1c1917}
.hover\:text-stone-900{color:#1c1917}
.hover\:bg-stone-950{background-color:#0c0a09}
.hover\:text-stone-950{color:#0c0a09}
.hover\:bg-green-50{background-color:#f0fdf4}
.hover\:text-green-50{color:#f0fdf4}
.hover\:bg-green-100{background-color:#dcfce7}
.hover\:text-green-100{color:#dcfce7}
.hover\:bg-green-200{background-color:#bbf7d0}
.hover\:text-green-200{color:#bbf7d0}
.hover\:bg-green-300{background-color:#86efac}
.hover\:text-green-300{color:#86efac}
.hover\:bg-green-400{background-color:#4ade80}
.hover\:text-green-400{color:#4ade80}
.hover\:bg-green-600{background-color:#16a34a}
.hover\:text-green-600{color:#16a34a}
.hover\:bg-green-700{background-color:#15803d}
.hover\:text-green-700{color:#15803d}
.hover\:bg-green-800{background-color:#166534}
.hover\:text-green-800{color:#166534}
.hover\:bg-green-900{background-color:#14532d}
.hover\:text-green-900{color:#14532d}
.hover\:bg-green-950{background-color:#052e16}
.hover\:text-green-950{color:#052e16}
.hover\:bg-blue-50{background-color:#eff6ff}
.hover\:text-blue-50{color:#eff6ff}
.hover\:bg-blue-100{background-color:#dbeafe}
.hover\:text-blue-100{color:#dbeafe}
.hover\:bg-blue-200{background-color:#bfdbfe}
.hover\:text-blue-200{color:#bfdbfe}
.hover\:bg-blue-600{background-color:#2563eb}
.hover\:text-blue-600{color:#2563eb}
.hover\:bg-blue-700{background-color:#1d4ed8}
.hover\:text-blue-700{color:#1d4ed8}
.hover\:bg-red-50{background-color:#fef2f2}
.hover\:text-red-50{color:#fef2f2}
.hover\:bg-red-100{background-color:#fee2e2}
.hover\:text-red-100{color:#fee2e2}
.hover\:bg-red-200{background-color:#fecaca}
.hover\:text-red-200{color:#fecaca}
.hover\:bg-red-600{background-color:#dc2626}
.hover\:text-red-600{color:#dc2626}
.hover\:bg-red-700{background-color:#b91c1c}
.hover\:text-red-700{color:#b91c1c}
.hover\:bg-amber-50{background-color:#fffbeb}
.hover\:text-amber-50{color:#fffbeb}
.hover\:bg-amber-100{background-color:#fef3c7}
.hover\:text-amber-100{color:#fef3c7}
.hover\:bg-amber-200{background-color:#fde68a}
.hover\:text-amber-200{color:#fde68a}
.hover\:bg-amber-400{background-color:#fbbf24}
.hover\:text-amber-400{color:#fbbf24}
.hover\:bg-amber-600{background-color:#d97706}
.hover\:text-amber-600{color:#d97706}
.hover\:bg-amber-700{background-color:#b45309}
.hover\:text-amber-700{color:#b45309}
.hover\:bg-amber-800{background-color:#92400e}
.hover\:text-amber-800{color:#92400e}
.hover\:bg-white{background-color:#ffffff}
.hover\:text-white{color:#ffffff}
.focus\:outline-none{outline:2px solid transparent;outline-offset:2px}
.focus\:ring-2{--tw-ring-shadow:0 0 0 2px var(--tw-ring-color)}
.focus\:ring-green-600{}
.focus\:ring-green-600:focus{box-shadow:0 0 0 2px #16a34a}
.focus\:outline-none:focus{outline:none}
.disabled\:opacity-60{}
.disabled\:bg-stone-300{}
.disabled\:opacity-60:disabled{opacity:0.6}
.disabled\:bg-stone-300:disabled{background-color:#d6d3d1}
.hover\:underline:hover{text-decoration:underline}
.col-span-2{grid-column:span 2/span 2}
.col-span-3{grid-column:span 3/span 3}
@media(min-width:640px){
.sm\:grid-cols-2{grid-template-columns:repeat(2,minmax(0,1fr))}
.sm\:grid-cols-3{grid-template-columns:repeat(3,minmax(0,1fr))}
.sm\:col-span-2{grid-column:span 2/span 2}
.sm\:p-6{padding:1.5rem}
}@media(min-width:768px){
.md\:block{display:block}
.md\:hidden{display:none}
.md\:flex{display:flex}
.md\:flex-col{flex-direction:column}
.md\:flex-row{flex-direction:row}
.md\:flex-1{flex:1 1 0%}
.md\:fixed{position:fixed}
.md\:top-0{top:0}
.md\:left-0{left:0}
.md\:h-screen{height:100vh}
.md\:w-60{width:15rem}
.md\:ml-60{margin-left:15rem}
.md\:px-3{padding-left:0.75rem;padding-right:0.75rem}
.md\:py-4{padding-top:1rem;padding-bottom:1rem}
.md\:overflow-visible{overflow:visible}
}@media(min-width:1024px){
.lg\:grid-cols-3{grid-template-columns:repeat(3,minmax(0,1fr))}
.lg\:grid-cols-4{grid-template-columns:repeat(4,minmax(0,1fr))}
.lg\:p-8{padding:2rem}
}
</style>
</head>
<body>
<div id="root"></div>

<script>
if ('serviceWorker' in navigator) {
  const swCode = `const CACHE = 'rrfarm-v1';
const SHELL = ['/'];

self.addEventListener('install', e => {
  e.waitUntil(
    caches.open(CACHE).then(cache => cache.addAll(SHELL)).then(() => self.skipWaiting())
  );
});

self.addEventListener('activate', e => {
  e.waitUntil(
    caches.keys().then(keys =>
      Promise.all(keys.filter(k => k !== CACHE).map(k => caches.delete(k)))
    ).then(() => self.clients.claim())
  );
});

self.addEventListener('fetch', e => {
  // Only cache same-origin requests (not Firebase / gstatic)
  if (!e.request.url.startsWith(self.location.origin)) return;
  e.respondWith(
    caches.open(CACHE).then(cache =>
      cache.match(e.request).then(cached => {
        const network = fetch(e.request).then(resp => {
          cache.put(e.request, resp.clone());
          return resp;
        });
        return cached || network;
      })
    )
  );
});
`;
  const blob = new Blob([swCode], {type:'application/javascript'});
  navigator.serviceWorker.register(URL.createObjectURL(blob)).catch(()=>{});
}
</script>

<script type="module">

  import { initializeApp } from 'https://www.gstatic.com/firebasejs/12.15.0/firebase-app.js';
  import {
    getFirestore, collection, doc, setDoc, addDoc, updateDoc, deleteDoc, onSnapshot, runTransaction,
  } from 'https://www.gstatic.com/firebasejs/12.15.0/firebase-firestore.js';
  import { getAuth, signInAnonymously, onAuthStateChanged } from 'https://www.gstatic.com/firebasejs/12.15.0/firebase-auth.js';

  const firebaseConfig = {
    apiKey: "AIzaSyAPKpbTkm6XbLzP_QJkhi-FWqjxbTOWd58",
    authDomain: "rrfarm-193c4.firebaseapp.com",
    projectId: "rrfarm-193c4",
    storageBucket: "rrfarm-193c4.firebasestorage.app",
    messagingSenderId: "1088257121685",
    appId: "1:1088257121685:web:b8a9729720a2a77e91ea9c",
  };

  try {
    const app  = initializeApp(firebaseConfig);
    const db   = getFirestore(app);
    const auth = getAuth(app);
    window.fb  = { db, collection, doc, setDoc, addDoc, updateDoc, deleteDoc, onSnapshot, runTransaction };
    onAuthStateChanged(auth, (user) => {
      if (user) { window.__fbReady = true; window.dispatchEvent(new Event('firebase-ready')); }
    });
    signInAnonymously(auth).catch((err) =>
      window.dispatchEvent(new CustomEvent('firebase-auth-error', { detail: { message: err.message } }))
    );
  } catch (err) {
    window.dispatchEvent(new CustomEvent('firebase-auth-error', { detail: { message: err.message } }));
  }

</script>

<script>
(()=>{var Om=Object.create;var Hi=Object.defineProperty;var _m=Object.getOwnPropertyDescriptor;var Mm=Object.getOwnPropertyNames;var Dm=Object.getPrototypeOf,Um=Object.prototype.hasOwnProperty;var At=(l,t)=>()=>(t||l((t={exports:{}}).exports,t),t.exports);var Hm=(l,t,u,a)=>{if(t&&typeof t=="object"||typeof t=="function")for(let n of Mm(t))!Um.call(l,n)&&n!==u&&Hi(l,n,{get:()=>t[n],enumerable:!(a=_m(t,n))||a.enumerable});return l};var Ni=(l,t,u)=>(u=l!=null?Om(Dm(l)):{},Hm(t||!l||!l.__esModule?Hi(u,"default",{value:l,enumerable:!0}):u,l));var ji=At(_=>{"use strict";var Ke=Symbol.for("react.transitional.element"),Nm=Symbol.for("react.portal"),pm=Symbol.for("react.fragment"),qm=Symbol.for("react.strict_mode"),Bm=Symbol.for("react.profiler"),Ym=Symbol.for("react.consumer"),Rm=Symbol.for("react.context"),Cm=Symbol.for("react.forward_ref"),Gm=Symbol.for("react.suspense"),Xm=Symbol.for("react.memo"),Ri=Symbol.for("react.lazy"),Qm=Symbol.for("react.activity"),pi=Symbol.iterator;function Zm(l){return l===null||typeof l!="object"?null:(l=pi&&l[pi]||l["@@iterator"],typeof l=="function"?l:null)}var Ci={isMounted:function(){return!1},enqueueForceUpdate:function(){},enqueueReplaceState:function(){},enqueueSetState:function(){}},Gi=Object.assign,Xi={};function bu(l,t,u){this.props=l,this.context=t,this.refs=Xi,this.updater=u||Ci}bu.prototype.isReactComponent={};bu.prototype.setState=function(l,t){if(typeof l!="object"&&typeof l!="function"&&l!=null)throw Error("takes an object of state variables to update or a function which returns an object of state variables.");this.updater.enqueueSetState(this,l,t,"setState")};bu.prototype.forceUpdate=function(l){this.updater.enqueueForceUpdate(this,l,"forceUpdate")};function Qi(){}Qi.prototype=bu.prototype;function Je(l,t,u){this.props=l,this.context=t,this.refs=Xi,this.updater=u||Ci}var re=Je.prototype=new Qi;re.constructor=Je;Gi(re,bu.prototype);re.isPureReactComponent=!0;var qi=Array.isArray;function Le(){}var L={H:null,A:null,T:null,S:null},Zi=Object.prototype.hasOwnProperty;function we(l,t,u){var a=u.ref;return{$$typeof:Ke,type:l,key:t,ref:a!==void 0?a:null,props:u}}function jm(l,t){return we(l.type,t,l.props)}function We(l){return typeof l=="object"&&l!==null&&l.$$typeof===Ke}function Vm(l){var t={"=":"=0",":":"=2"};return"$"+l.replace(/[=:]/g,function(u){return t[u]})}var Bi=/\/+/g;function xe(l,t){return typeof l=="object"&&l!==null&&l.key!=null?Vm(""+l.key):t.toString(36)}function xm(l){switch(l.status){case"fulfilled":return l.value;case"rejected":throw l.reason;default:switch(typeof l.status=="string"?l.then(Le,Le):(l.status="pending",l.then(function(t){l.status==="pending"&&(l.status="fulfilled",l.value=t)},function(t){l.status==="pending"&&(l.status="rejected",l.reason=t)})),l.status){case"fulfilled":return l.value;case"rejected":throw l.reason}}throw l}function su(l,t,u,a,n){var e=typeof l;(e==="undefined"||e==="boolean")&&(l=null);var f=!1;if(l===null)f=!0;else switch(e){case"bigint":case"string":case"number":f=!0;break;case"object":switch(l.$$typeof){case Ke:case Nm:f=!0;break;case Ri:return f=l._init,su(f(l._payload),t,u,a,n)}}if(f)return n=n(l),f=a===""?"."+xe(l,0):a,qi(n)?(u="",f!=null&&(u=f.replace(Bi,"$&/")+"/"),su(n,t,u,"",function(m){return m})):n!=null&&(We(n)&&(n=jm(n,u+(n.key==null||l&&l.key===n.key?"":(""+n.key).replace(Bi,"$&/")+"/")+f)),t.push(n)),1;f=0;var c=a===""?".":a+":";if(qi(l))for(var i=0;i<l.length;i++)a=l[i],e=c+xe(a,i),f+=su(a,t,u,e,n);else if(i=Zm(l),typeof i=="function")for(l=i.call(l),i=0;!(a=l.next()).done;)a=a.value,e=c+xe(a,i++),f+=su(a,t,u,e,n);else if(e==="object"){if(typeof l.then=="function")return su(xm(l),t,u,a,n);throw t=String(l),Error("Objects are not valid as a React child (found: "+(t==="[object Object]"?"object with keys {"+Object.keys(l).join(", ")+"}":t)+"). If you meant to render a collection of children, use an array instead.")}return f}function mn(l,t,u){if(l==null)return l;var a=[],n=0;return su(l,a,"","",function(e){return t.call(u,e,n++)}),a}function Lm(l){if(l._status===-1){var t=l._result;t=t(),t.then(function(u){(l._status===0||l._status===-1)&&(l._status=1,l._result=u)},function(u){(l._status===0||l._status===-1)&&(l._status=2,l._result=u)}),l._status===-1&&(l._status=0,l._result=t)}if(l._status===1)return l._result.default;throw l._result}var Yi=typeof reportError=="function"?reportError:function(l){if(typeof window=="object"&&typeof window.ErrorEvent=="function"){var t=new window.ErrorEvent("error",{bubbles:!0,cancelable:!0,message:typeof l=="object"&&l!==null&&typeof l.message=="string"?String(l.message):String(l),error:l});if(!window.dispatchEvent(t))return}else if(typeof process=="object"&&typeof process.emit=="function"){process.emit("uncaughtException",l);return}console.error(l)},Km={map:mn,forEach:function(l,t,u){mn(l,function(){t.apply(this,arguments)},u)},count:function(l){var t=0;return mn(l,function(){t++}),t},toArray:function(l){return mn(l,function(t){return t})||[]},only:function(l){if(!We(l))throw Error("React.Children.only expected to receive a single React element child.");return l}};_.Activity=Qm;_.Children=Km;_.Component=bu;_.Fragment=pm;_.Profiler=Bm;_.PureComponent=Je;_.StrictMode=qm;_.Suspense=Gm;_.__CLIENT_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE=L;_.__COMPILER_RUNTIME={__proto__:null,c:function(l){return L.H.useMemoCache(l)}};_.cache=function(l){return function(){return l.apply(null,arguments)}};_.cacheSignal=function(){return null};_.cloneElement=function(l,t,u){if(l==null)throw Error("The argument must be a React element, but you passed "+l+".");var a=Gi({},l.props),n=l.key;if(t!=null)for(e in t.key!==void 0&&(n=""+t.key),t)!Zi.call(t,e)||e==="key"||e==="__self"||e==="__source"||e==="ref"&&t.ref===void 0||(a[e]=t[e]);var e=arguments.length-2;if(e===1)a.children=u;else if(1<e){for(var f=Array(e),c=0;c<e;c++)f[c]=arguments[c+2];a.children=f}return we(l.type,n,a)};_.createContext=function(l){return l={$$typeof:Rm,_currentValue:l,_currentValue2:l,_threadCount:0,Provider:null,Consumer:null},l.Provider=l,l.Consumer={$$typeof:Ym,_context:l},l};_.createElement=function(l,t,u){var a,n={},e=null;if(t!=null)for(a in t.key!==void 0&&(e=""+t.key),t)Zi.call(t,a)&&a!=="key"&&a!=="__self"&&a!=="__source"&&(n[a]=t[a]);var f=arguments.length-2;if(f===1)n.children=u;else if(1<f){for(var c=Array(f),i=0;i<f;i++)c[i]=arguments[i+2];n.children=c}if(l&&l.defaultProps)for(a in f=l.defaultProps,f)n[a]===void 0&&(n[a]=f[a]);return we(l,e,n)};_.createRef=function(){return{current:null}};_.forwardRef=function(l){return{$$typeof:Cm,render:l}};_.isValidElement=We;_.lazy=function(l){return{$$typeof:Ri,_payload:{_status:-1,_result:l},_init:Lm}};_.memo=function(l,t){return{$$typeof:Xm,type:l,compare:t===void 0?null:t}};_.startTransition=function(l){var t=L.T,u={};L.T=u;try{var a=l(),n=L.S;n!==null&&n(u,a),typeof a=="object"&&a!==null&&typeof a.then=="function"&&a.then(Le,Yi)}catch(e){Yi(e)}finally{t!==null&&u.types!==null&&(t.types=u.types),L.T=t}};_.unstable_useCacheRefresh=function(){return L.H.useCacheRefresh()};_.use=function(l){return L.H.use(l)};_.useActionState=function(l,t,u){return L.H.useActionState(l,t,u)};_.useCallback=function(l,t){return L.H.useCallback(l,t)};_.useContext=function(l){return L.H.useContext(l)};_.useDebugValue=function(){};_.useDeferredValue=function(l,t){return L.H.useDeferredValue(l,t)};_.useEffect=function(l,t){return L.H.useEffect(l,t)};_.useEffectEvent=function(l){return L.H.useEffectEvent(l)};_.useId=function(){return L.H.useId()};_.useImperativeHandle=function(l,t,u){return L.H.useImperativeHandle(l,t,u)};_.useInsertionEffect=function(l,t){return L.H.useInsertionEffect(l,t)};_.useLayoutEffect=function(l,t){return L.H.useLayoutEffect(l,t)};_.useMemo=function(l,t){return L.H.useMemo(l,t)};_.useOptimistic=function(l,t){return L.H.useOptimistic(l,t)};_.useReducer=function(l,t,u){return L.H.useReducer(l,t,u)};_.useRef=function(l){return L.H.useRef(l)};_.useState=function(l){return L.H.useState(l)};_.useSyncExternalStore=function(l,t,u){return L.H.useSyncExternalStore(l,t,u)};_.useTransition=function(){return L.H.useTransition()};_.version="19.2.5"});var dn=At((A2,Vi)=>{"use strict";Vi.exports=ji()});var ki=At(w=>{"use strict";function Ie(l,t){var u=l.length;l.push(t);l:for(;0<u;){var a=u-1>>>1,n=l[a];if(0<hn(n,t))l[a]=t,l[u]=n,u=a;else break l}}function Wl(l){return l.length===0?null:l[0]}function gn(l){if(l.length===0)return null;var t=l[0],u=l.pop();if(u!==t){l[0]=u;l:for(var a=0,n=l.length,e=n>>>1;a<e;){var f=2*(a+1)-1,c=l[f],i=f+1,m=l[i];if(0>hn(c,u))i<n&&0>hn(m,c)?(l[a]=m,l[i]=u,a=i):(l[a]=c,l[f]=u,a=f);else if(i<n&&0>hn(m,u))l[a]=m,l[i]=u,a=i;else break l}}return t}function hn(l,t){var u=l.sortIndex-t.sortIndex;return u!==0?u:l.id-t.id}w.unstable_now=void 0;typeof performance=="object"&&typeof performance.now=="function"?(xi=performance,w.unstable_now=function(){return xi.now()}):($e=Date,Li=$e.now(),w.unstable_now=function(){return $e.now()-Li});var xi,$e,Li,tt=[],Ot=[],Jm=1,Rl=null,hl=3,Pe=!1,ya=!1,va=!1,lf=!1,ri=typeof setTimeout=="function"?setTimeout:null,wi=typeof clearTimeout=="function"?clearTimeout:null,Ki=typeof setImmediate<"u"?setImmediate:null;function Sn(l){for(var t=Wl(Ot);t!==null;){if(t.callback===null)gn(Ot);else if(t.startTime<=l)gn(Ot),t.sortIndex=t.expirationTime,Ie(tt,t);else break;t=Wl(Ot)}}function tf(l){if(va=!1,Sn(l),!ya)if(Wl(tt)!==null)ya=!0,Eu||(Eu=!0,zu());else{var t=Wl(Ot);t!==null&&uf(tf,t.startTime-l)}}var Eu=!1,ma=-1,Wi=5,$i=-1;function Fi(){return lf?!0:!(w.unstable_now()-$i<Wi)}function Fe(){if(lf=!1,Eu){var l=w.unstable_now();$i=l;var t=!0;try{l:{ya=!1,va&&(va=!1,wi(ma),ma=-1),Pe=!0;var u=hl;try{t:{for(Sn(l),Rl=Wl(tt);Rl!==null&&!(Rl.expirationTime>l&&Fi());){var a=Rl.callback;if(typeof a=="function"){Rl.callback=null,hl=Rl.priorityLevel;var n=a(Rl.expirationTime<=l);if(l=w.unstable_now(),typeof n=="function"){Rl.callback=n,Sn(l),t=!0;break t}Rl===Wl(tt)&&gn(tt),Sn(l)}else gn(tt);Rl=Wl(tt)}if(Rl!==null)t=!0;else{var e=Wl(Ot);e!==null&&uf(tf,e.startTime-l),t=!1}}break l}finally{Rl=null,hl=u,Pe=!1}t=void 0}}finally{t?zu():Eu=!1}}}var zu;typeof Ki=="function"?zu=function(){Ki(Fe)}:typeof MessageChannel<"u"?(ke=new MessageChannel,Ji=ke.port2,ke.port1.onmessage=Fe,zu=function(){Ji.postMessage(null)}):zu=function(){ri(Fe,0)};var ke,Ji;function uf(l,t){ma=ri(function(){l(w.unstable_now())},t)}w.unstable_IdlePriority=5;w.unstable_ImmediatePriority=1;w.unstable_LowPriority=4;w.unstable_NormalPriority=3;w.unstable_Profiling=null;w.unstable_UserBlockingPriority=2;w.unstable_cancelCallback=function(l){l.callback=null};w.unstable_forceFrameRate=function(l){0>l||125<l?console.error("forceFrameRate takes a positive int between 0 and 125, forcing frame rates higher than 125 fps is not supported"):Wi=0<l?Math.floor(1e3/l):5};w.unstable_getCurrentPriorityLevel=function(){return hl};w.unstable_next=function(l){switch(hl){case 1:case 2:case 3:var t=3;break;default:t=hl}var u=hl;hl=t;try{return l()}finally{hl=u}};w.unstable_requestPaint=function(){lf=!0};w.unstable_runWithPriority=function(l,t){switch(l){case 1:case 2:case 3:case 4:case 5:break;default:l=3}var u=hl;hl=l;try{return t()}finally{hl=u}};w.unstable_scheduleCallback=function(l,t,u){var a=w.unstable_now();switch(typeof u=="object"&&u!==null?(u=u.delay,u=typeof u=="number"&&0<u?a+u:a):u=a,l){case 1:var n=-1;break;case 2:n=250;break;case 5:n=1073741823;break;case 4:n=1e4;break;default:n=5e3}return n=u+n,l={id:Jm++,callback:t,priorityLevel:l,startTime:u,expirationTime:n,sortIndex:-1},u>a?(l.sortIndex=u,Ie(Ot,l),Wl(tt)===null&&l===Wl(Ot)&&(va?(wi(ma),ma=-1):va=!0,uf(tf,u-a))):(l.sortIndex=n,Ie(tt,l),ya||Pe||(ya=!0,Eu||(Eu=!0,zu()))),l};w.unstable_shouldYield=Fi;w.unstable_wrapCallback=function(l){var t=hl;return function(){var u=hl;hl=t;try{return l.apply(this,arguments)}finally{hl=u}}}});var Pi=At((_2,Ii)=>{"use strict";Ii.exports=ki()});var t0=At(gl=>{"use strict";var rm=dn();function l0(l){var t="https://react.dev/errors/"+l;if(1<arguments.length){t+="?args[]="+encodeURIComponent(arguments[1]);for(var u=2;u<arguments.length;u++)t+="&args[]="+encodeURIComponent(arguments[u])}return"Minified React error #"+l+"; visit "+t+" for the full message or use the non-minified dev environment for full errors and additional helpful warnings."}function _t(){}var Sl={d:{f:_t,r:function(){throw Error(l0(522))},D:_t,C:_t,L:_t,m:_t,X:_t,S:_t,M:_t},p:0,findDOMNode:null},wm=Symbol.for("react.portal");function Wm(l,t,u){var a=3<arguments.length&&arguments[3]!==void 0?arguments[3]:null;return{$$typeof:wm,key:a==null?null:""+a,children:l,containerInfo:t,implementation:u}}var da=rm.__CLIENT_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE;function on(l,t){if(l==="font")return"";if(typeof t=="string")return t==="use-credentials"?t:""}gl.__DOM_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE=Sl;gl.createPortal=function(l,t){var u=2<arguments.length&&arguments[2]!==void 0?arguments[2]:null;if(!t||t.nodeType!==1&&t.nodeType!==9&&t.nodeType!==11)throw Error(l0(299));return Wm(l,t,null,u)};gl.flushSync=function(l){var t=da.T,u=Sl.p;try{if(da.T=null,Sl.p=2,l)return l()}finally{da.T=t,Sl.p=u,Sl.d.f()}};gl.preconnect=function(l,t){typeof l=="string"&&(t?(t=t.crossOrigin,t=typeof t=="string"?t==="use-credentials"?t:"":void 0):t=null,Sl.d.C(l,t))};gl.prefetchDNS=function(l){typeof l=="string"&&Sl.d.D(l)};gl.preinit=function(l,t){if(typeof l=="string"&&t&&typeof t.as=="string"){var u=t.as,a=on(u,t.crossOrigin),n=typeof t.integrity=="string"?t.integrity:void 0,e=typeof t.fetchPriority=="string"?t.fetchPriority:void 0;u==="style"?Sl.d.S(l,typeof t.precedence=="string"?t.precedence:void 0,{crossOrigin:a,integrity:n,fetchPriority:e}):u==="script"&&Sl.d.X(l,{crossOrigin:a,integrity:n,fetchPriority:e,nonce:typeof t.nonce=="string"?t.nonce:void 0})}};gl.preinitModule=function(l,t){if(typeof l=="string")if(typeof t=="object"&&t!==null){if(t.as==null||t.as==="script"){var u=on(t.as,t.crossOrigin);Sl.d.M(l,{crossOrigin:u,integrity:typeof t.integrity=="string"?t.integrity:void 0,nonce:typeof t.nonce=="string"?t.nonce:void 0})}}else t==null&&Sl.d.M(l)};gl.preload=function(l,t){if(typeof l=="string"&&typeof t=="object"&&t!==null&&typeof t.as=="string"){var u=t.as,a=on(u,t.crossOrigin);Sl.d.L(l,u,{crossOrigin:a,integrity:typeof t.integrity=="string"?t.integrity:void 0,nonce:typeof t.nonce=="string"?t.nonce:void 0,type:typeof t.type=="string"?t.type:void 0,fetchPriority:typeof t.fetchPriority=="string"?t.fetchPriority:void 0,referrerPolicy:typeof t.referrerPolicy=="string"?t.referrerPolicy:void 0,imageSrcSet:typeof t.imageSrcSet=="string"?t.imageSrcSet:void 0,imageSizes:typeof t.imageSizes=="string"?t.imageSizes:void 0,media:typeof t.media=="string"?t.media:void 0})}};gl.preloadModule=function(l,t){if(typeof l=="string")if(t){var u=on(t.as,t.crossOrigin);Sl.d.m(l,{as:typeof t.as=="string"&&t.as!=="script"?t.as:void 0,crossOrigin:u,integrity:typeof t.integrity=="string"?t.integrity:void 0})}else Sl.d.m(l)};gl.requestFormReset=function(l){Sl.d.r(l)};gl.unstable_batchedUpdates=function(l,t){return l(t)};gl.useFormState=function(l,t,u){return da.H.useFormState(l,t,u)};gl.useFormStatus=function(){return da.H.useHostTransitionStatus()};gl.version="19.2.5"});var n0=At((D2,a0)=>{"use strict";function u0(){if(!(typeof __REACT_DEVTOOLS_GLOBAL_HOOK__>"u"||typeof __REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE!="function"))try{__REACT_DEVTOOLS_GLOBAL_HOOK__.checkDCE(u0)}catch(l){console.error(l)}}u0(),a0.exports=t0()});var om=At(Ve=>{"use strict";var nl=Pi(),p1=dn(),$m=n0();function b(l){var t="https://react.dev/errors/"+l;if(1<arguments.length){t+="?args[]="+encodeURIComponent(arguments[1]);for(var u=2;u<arguments.length;u++)t+="&args[]="+encodeURIComponent(arguments[u])}return"Minified React error #"+l+"; visit "+t+" for the full message or use the non-minified dev environment for full errors and additional helpful warnings."}function q1(l){return!(!l||l.nodeType!==1&&l.nodeType!==9&&l.nodeType!==11)}function Ia(l){var t=l,u=l;if(l.alternate)for(;t.return;)t=t.return;else{l=t;do t=l,(t.flags&4098)!==0&&(u=t.return),l=t.return;while(l)}return t.tag===3?u:null}function B1(l){if(l.tag===13){var t=l.memoizedState;if(t===null&&(l=l.alternate,l!==null&&(t=l.memoizedState)),t!==null)return t.dehydrated}return null}function Y1(l){if(l.tag===31){var t=l.memoizedState;if(t===null&&(l=l.alternate,l!==null&&(t=l.memoizedState)),t!==null)return t.dehydrated}return null}function e0(l){if(Ia(l)!==l)throw Error(b(188))}function Fm(l){var t=l.alternate;if(!t){if(t=Ia(l),t===null)throw Error(b(188));return t!==l?null:l}for(var u=l,a=t;;){var n=u.return;if(n===null)break;var e=n.alternate;if(e===null){if(a=n.return,a!==null){u=a;continue}break}if(n.child===e.child){for(e=n.child;e;){if(e===u)return e0(n),l;if(e===a)return e0(n),t;e=e.sibling}throw Error(b(188))}if(u.return!==a.return)u=n,a=e;else{for(var f=!1,c=n.child;c;){if(c===u){f=!0,u=n,a=e;break}if(c===a){f=!0,a=n,u=e;break}c=c.sibling}if(!f){for(c=e.child;c;){if(c===u){f=!0,u=e,a=n;break}if(c===a){f=!0,a=e,u=n;break}c=c.sibling}if(!f)throw Error(b(189))}}if(u.alternate!==a)throw Error(b(190))}if(u.tag!==3)throw Error(b(188));return u.stateNode.current===u?l:t}function R1(l){var t=l.tag;if(t===5||t===26||t===27||t===6)return l;for(l=l.child;l!==null;){if(t=R1(l),t!==null)return t;l=l.sibling}return null}var r=Object.assign,km=Symbol.for("react.element"),sn=Symbol.for("react.transitional.element"),Ea=Symbol.for("react.portal"),Du=Symbol.for("react.fragment"),C1=Symbol.for("react.strict_mode"),Xf=Symbol.for("react.profiler"),G1=Symbol.for("react.consumer"),yt=Symbol.for("react.context"),Bc=Symbol.for("react.forward_ref"),Qf=Symbol.for("react.suspense"),Zf=Symbol.for("react.suspense_list"),Yc=Symbol.for("react.memo"),Mt=Symbol.for("react.lazy"),jf=Symbol.for("react.activity"),Im=Symbol.for("react.memo_cache_sentinel"),f0=Symbol.iterator;function ha(l){return l===null||typeof l!="object"?null:(l=f0&&l[f0]||l["@@iterator"],typeof l=="function"?l:null)}var Pm=Symbol.for("react.client.reference");function Vf(l){if(l==null)return null;if(typeof l=="function")return l.$$typeof===Pm?null:l.displayName||l.name||null;if(typeof l=="string")return l;switch(l){case Du:return"Fragment";case Xf:return"Profiler";case C1:return"StrictMode";case Qf:return"Suspense";case Zf:return"SuspenseList";case jf:return"Activity"}if(typeof l=="object")switch(l.$$typeof){case Ea:return"Portal";case yt:return l.displayName||"Context";case G1:return(l._context.displayName||"Context")+".Consumer";case Bc:var t=l.render;return l=l.displayName,l||(l=t.displayName||t.name||"",l=l!==""?"ForwardRef("+l+")":"ForwardRef"),l;case Yc:return t=l.displayName||null,t!==null?t:Vf(l.type)||"Memo";case Mt:t=l._payload,l=l._init;try{return Vf(l(t))}catch{}}return null}var Ta=Array.isArray,O=p1.__CLIENT_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE,C=$m.__DOM_INTERNALS_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE,uu={pending:!1,data:null,method:null,action:null},xf=[],Uu=-1;function Pl(l){return{current:l}}function cl(l){0>Uu||(l.current=xf[Uu],xf[Uu]=null,Uu--)}function x(l,t){Uu++,xf[Uu]=l.current,l.current=t}var Il=Pl(null),Qa=Pl(null),Gt=Pl(null),Fn=Pl(null);function kn(l,t){switch(x(Gt,t),x(Qa,l),x(Il,null),t.nodeType){case 9:case 11:l=(l=t.documentElement)&&(l=l.namespaceURI)?h1(l):0;break;default:if(l=t.tagName,t=t.namespaceURI)t=h1(t),l=um(t,l);else switch(l){case"svg":l=1;break;case"math":l=2;break;default:l=0}}cl(Il),x(Il,l)}function Ju(){cl(Il),cl(Qa),cl(Gt)}function Lf(l){l.memoizedState!==null&&x(Fn,l);var t=Il.current,u=um(t,l.type);t!==u&&(x(Qa,l),x(Il,u))}function In(l){Qa.current===l&&(cl(Il),cl(Qa)),Fn.current===l&&(cl(Fn),$a._currentValue=uu)}var af,c0;function It(l){if(af===void 0)try{throw Error()}catch(u){var t=u.stack.trim().match(/\n( *(at )?)/);af=t&&t[1]||"",c0=-1<u.stack.indexOf(`
    at`)?" (<anonymous>)":-1<u.stack.indexOf("@")?"@unknown:0:0":""}return`
`+af+l+c0}var nf=!1;function ef(l,t){if(!l||nf)return"";nf=!0;var u=Error.prepareStackTrace;Error.prepareStackTrace=void 0;try{var a={DetermineComponentFrameRoot:function(){try{if(t){var s=function(){throw Error()};if(Object.defineProperty(s.prototype,"props",{set:function(){throw Error()}}),typeof Reflect=="object"&&Reflect.construct){try{Reflect.construct(s,[])}catch(S){var h=S}Reflect.construct(l,[],s)}else{try{s.call()}catch(S){h=S}l.call(s.prototype)}}else{try{throw Error()}catch(S){h=S}(s=l())&&typeof s.catch=="function"&&s.catch(function(){})}}catch(S){if(S&&h&&typeof S.stack=="string")return[S.stack,h.stack]}return[null,null]}};a.DetermineComponentFrameRoot.displayName="DetermineComponentFrameRoot";var n=Object.getOwnPropertyDescriptor(a.DetermineComponentFrameRoot,"name");n&&n.configurable&&Object.defineProperty(a.DetermineComponentFrameRoot,"name",{value:"DetermineComponentFrameRoot"});var e=a.DetermineComponentFrameRoot(),f=e[0],c=e[1];if(f&&c){var i=f.split(`
`),m=c.split(`
`);for(n=a=0;a<i.length&&!i[a].includes("DetermineComponentFrameRoot");)a++;for(;n<m.length&&!m[n].includes("DetermineComponentFrameRoot");)n++;if(a===i.length||n===m.length)for(a=i.length-1,n=m.length-1;1<=a&&0<=n&&i[a]!==m[n];)n--;for(;1<=a&&0<=n;a--,n--)if(i[a]!==m[n]){if(a!==1||n!==1)do if(a--,n--,0>n||i[a]!==m[n]){var g=`
`+i[a].replace(" at new "," at ");return l.displayName&&g.includes("<anonymous>")&&(g=g.replace("<anonymous>",l.displayName)),g}while(1<=a&&0<=n);break}}}finally{nf=!1,Error.prepareStackTrace=u}return(u=l?l.displayName||l.name:"")?It(u):""}function ld(l,t){switch(l.tag){case 26:case 27:case 5:return It(l.type);case 16:return It("Lazy");case 13:return l.child!==t&&t!==null?It("Suspense Fallback"):It("Suspense");case 19:return It("SuspenseList");case 0:case 15:return ef(l.type,!1);case 11:return ef(l.type.render,!1);case 1:return ef(l.type,!0);case 31:return It("Activity");default:return""}}function i0(l){try{var t="",u=null;do t+=ld(l,u),u=l,l=l.return;while(l);return t}catch(a){return`
Error generating stack: `+a.message+`
`+a.stack}}var Kf=Object.prototype.hasOwnProperty,Rc=nl.unstable_scheduleCallback,ff=nl.unstable_cancelCallback,td=nl.unstable_shouldYield,ud=nl.unstable_requestPaint,Hl=nl.unstable_now,ad=nl.unstable_getCurrentPriorityLevel,X1=nl.unstable_ImmediatePriority,Q1=nl.unstable_UserBlockingPriority,Pn=nl.unstable_NormalPriority,nd=nl.unstable_LowPriority,Z1=nl.unstable_IdlePriority,ed=nl.log,fd=nl.unstable_setDisableYieldValue,Pa=null,Nl=null;function qt(l){if(typeof ed=="function"&&fd(l),Nl&&typeof Nl.setStrictMode=="function")try{Nl.setStrictMode(Pa,l)}catch{}}var pl=Math.clz32?Math.clz32:yd,cd=Math.log,id=Math.LN2;function yd(l){return l>>>=0,l===0?32:31-(cd(l)/id|0)|0}var bn=256,zn=262144,En=4194304;function Pt(l){var t=l&42;if(t!==0)return t;switch(l&-l){case 1:return 1;case 2:return 2;case 4:return 4;case 8:return 8;case 16:return 16;case 32:return 32;case 64:return 64;case 128:return 128;case 256:case 512:case 1024:case 2048:case 4096:case 8192:case 16384:case 32768:case 65536:case 131072:return l&261888;case 262144:case 524288:case 1048576:case 2097152:return l&3932160;case 4194304:case 8388608:case 16777216:case 33554432:return l&62914560;case 67108864:return 67108864;case 134217728:return 134217728;case 268435456:return 268435456;case 536870912:return 536870912;case 1073741824:return 0;default:return l}}function Me(l,t,u){var a=l.pendingLanes;if(a===0)return 0;var n=0,e=l.suspendedLanes,f=l.pingedLanes;l=l.warmLanes;var c=a&134217727;return c!==0?(a=c&~e,a!==0?n=Pt(a):(f&=c,f!==0?n=Pt(f):u||(u=c&~l,u!==0&&(n=Pt(u))))):(c=a&~e,c!==0?n=Pt(c):f!==0?n=Pt(f):u||(u=a&~l,u!==0&&(n=Pt(u)))),n===0?0:t!==0&&t!==n&&(t&e)===0&&(e=n&-n,u=t&-t,e>=u||e===32&&(u&4194048)!==0)?t:n}function ln(l,t){return(l.pendingLanes&~(l.suspendedLanes&~l.pingedLanes)&t)===0}function vd(l,t){switch(l){case 1:case 2:case 4:case 8:case 64:return t+250;case 16:case 32:case 128:case 256:case 512:case 1024:case 2048:case 4096:case 8192:case 16384:case 32768:case 65536:case 131072:case 262144:case 524288:case 1048576:case 2097152:return t+5e3;case 4194304:case 8388608:case 16777216:case 33554432:return-1;case 67108864:case 134217728:case 268435456:case 536870912:case 1073741824:return-1;default:return-1}}function j1(){var l=En;return En<<=1,(En&62914560)===0&&(En=4194304),l}function cf(l){for(var t=[],u=0;31>u;u++)t.push(l);return t}function tn(l,t){l.pendingLanes|=t,t!==268435456&&(l.suspendedLanes=0,l.pingedLanes=0,l.warmLanes=0)}function md(l,t,u,a,n,e){var f=l.pendingLanes;l.pendingLanes=u,l.suspendedLanes=0,l.pingedLanes=0,l.warmLanes=0,l.expiredLanes&=u,l.entangledLanes&=u,l.errorRecoveryDisabledLanes&=u,l.shellSuspendCounter=0;var c=l.entanglements,i=l.expirationTimes,m=l.hiddenUpdates;for(u=f&~u;0<u;){var g=31-pl(u),s=1<<g;c[g]=0,i[g]=-1;var h=m[g];if(h!==null)for(m[g]=null,g=0;g<h.length;g++){var S=h[g];S!==null&&(S.lane&=-536870913)}u&=~s}a!==0&&V1(l,a,0),e!==0&&n===0&&l.tag!==0&&(l.suspendedLanes|=e&~(f&~t))}function V1(l,t,u){l.pendingLanes|=t,l.suspendedLanes&=~t;var a=31-pl(t);l.entangledLanes|=t,l.entanglements[a]=l.entanglements[a]|1073741824|u&261930}function x1(l,t){var u=l.entangledLanes|=t;for(l=l.entanglements;u;){var a=31-pl(u),n=1<<a;n&t|l[a]&t&&(l[a]|=t),u&=~n}}function L1(l,t){var u=t&-t;return u=(u&42)!==0?1:Cc(u),(u&(l.suspendedLanes|t))!==0?0:u}function Cc(l){switch(l){case 2:l=1;break;case 8:l=4;break;case 32:l=16;break;case 256:case 512:case 1024:case 2048:case 4096:case 8192:case 16384:case 32768:case 65536:case 131072:case 262144:case 524288:case 1048576:case 2097152:case 4194304:case 8388608:case 16777216:case 33554432:l=128;break;case 268435456:l=134217728;break;default:l=0}return l}function Gc(l){return l&=-l,2<l?8<l?(l&134217727)!==0?32:268435456:8:2}function K1(){var l=C.p;return l!==0?l:(l=window.event,l===void 0?32:hm(l.type))}function y0(l,t){var u=C.p;try{return C.p=l,t()}finally{C.p=u}}var $t=Math.random().toString(36).slice(2),yl="__reactFiber$"+$t,Al="__reactProps$"+$t,ua="__reactContainer$"+$t,Jf="__reactEvents$"+$t,dd="__reactListeners$"+$t,hd="__reactHandles$"+$t,v0="__reactResources$"+$t,un="__reactMarker$"+$t;function Xc(l){delete l[yl],delete l[Al],delete l[Jf],delete l[dd],delete l[hd]}function Hu(l){var t=l[yl];if(t)return t;for(var u=l.parentNode;u;){if(t=u[ua]||u[yl]){if(u=t.alternate,t.child!==null||u!==null&&u.child!==null)for(l=b1(l);l!==null;){if(u=l[yl])return u;l=b1(l)}return t}l=u,u=l.parentNode}return null}function aa(l){if(l=l[yl]||l[ua]){var t=l.tag;if(t===5||t===6||t===13||t===31||t===26||t===27||t===3)return l}return null}function Aa(l){var t=l.tag;if(t===5||t===26||t===27||t===6)return l.stateNode;throw Error(b(33))}function Qu(l){var t=l[v0];return t||(t=l[v0]={hoistableStyles:new Map,hoistableScripts:new Map}),t}function fl(l){l[un]=!0}var J1=new Set,r1={};function du(l,t){ru(l,t),ru(l+"Capture",t)}function ru(l,t){for(r1[l]=t,l=0;l<t.length;l++)J1.add(t[l])}var Sd=RegExp("^[:A-Z_a-z\\u00C0-\\u00D6\\u00D8-\\u00F6\\u00F8-\\u02FF\\u0370-\\u037D\\u037F-\\u1FFF\\u200C-\\u200D\\u2070-\\u218F\\u2C00-\\u2FEF\\u3001-\\uD7FF\\uF900-\\uFDCF\\uFDF0-\\uFFFD][:A-Z_a-z\\u00C0-\\u00D6\\u00D8-\\u00F6\\u00F8-\\u02FF\\u0370-\\u037D\\u037F-\\u1FFF\\u200C-\\u200D\\u2070-\\u218F\\u2C00-\\u2FEF\\u3001-\\uD7FF\\uF900-\\uFDCF\\uFDF0-\\uFFFD\\-.0-9\\u00B7\\u0300-\\u036F\\u203F-\\u2040]*$"),m0={},d0={};function gd(l){return Kf.call(d0,l)?!0:Kf.call(m0,l)?!1:Sd.test(l)?d0[l]=!0:(m0[l]=!0,!1)}function Cn(l,t,u){if(gd(t))if(u===null)l.removeAttribute(t);else{switch(typeof u){case"undefined":case"function":case"symbol":l.removeAttribute(t);return;case"boolean":var a=t.toLowerCase().slice(0,5);if(a!=="data-"&&a!=="aria-"){l.removeAttribute(t);return}}l.setAttribute(t,""+u)}}function Tn(l,t,u){if(u===null)l.removeAttribute(t);else{switch(typeof u){case"undefined":case"function":case"symbol":case"boolean":l.removeAttribute(t);return}l.setAttribute(t,""+u)}}function ut(l,t,u,a){if(a===null)l.removeAttribute(u);else{switch(typeof a){case"undefined":case"function":case"symbol":case"boolean":l.removeAttribute(u);return}l.setAttributeNS(t,u,""+a)}}function Gl(l){switch(typeof l){case"bigint":case"boolean":case"number":case"string":case"undefined":return l;case"object":return l;default:return""}}function w1(l){var t=l.type;return(l=l.nodeName)&&l.toLowerCase()==="input"&&(t==="checkbox"||t==="radio")}function od(l,t,u){var a=Object.getOwnPropertyDescriptor(l.constructor.prototype,t);if(!l.hasOwnProperty(t)&&typeof a<"u"&&typeof a.get=="function"&&typeof a.set=="function"){var n=a.get,e=a.set;return Object.defineProperty(l,t,{configurable:!0,get:function(){return n.call(this)},set:function(f){u=""+f,e.call(this,f)}}),Object.defineProperty(l,t,{enumerable:a.enumerable}),{getValue:function(){return u},setValue:function(f){u=""+f},stopTracking:function(){l._valueTracker=null,delete l[t]}}}}function rf(l){if(!l._valueTracker){var t=w1(l)?"checked":"value";l._valueTracker=od(l,t,""+l[t])}}function W1(l){if(!l)return!1;var t=l._valueTracker;if(!t)return!0;var u=t.getValue(),a="";return l&&(a=w1(l)?l.checked?"true":"false":l.value),l=a,l!==u?(t.setValue(l),!0):!1}function le(l){if(l=l||(typeof document<"u"?document:void 0),typeof l>"u")return null;try{return l.activeElement||l.body}catch{return l.body}}var sd=/[\n"\\]/g;function Zl(l){return l.replace(sd,function(t){return"\\"+t.charCodeAt(0).toString(16)+" "})}function wf(l,t,u,a,n,e,f,c){l.name="",f!=null&&typeof f!="function"&&typeof f!="symbol"&&typeof f!="boolean"?l.type=f:l.removeAttribute("type"),t!=null?f==="number"?(t===0&&l.value===""||l.value!=t)&&(l.value=""+Gl(t)):l.value!==""+Gl(t)&&(l.value=""+Gl(t)):f!=="submit"&&f!=="reset"||l.removeAttribute("value"),t!=null?Wf(l,f,Gl(t)):u!=null?Wf(l,f,Gl(u)):a!=null&&l.removeAttribute("value"),n==null&&e!=null&&(l.defaultChecked=!!e),n!=null&&(l.checked=n&&typeof n!="function"&&typeof n!="symbol"),c!=null&&typeof c!="function"&&typeof c!="symbol"&&typeof c!="boolean"?l.name=""+Gl(c):l.removeAttribute("name")}function $1(l,t,u,a,n,e,f,c){if(e!=null&&typeof e!="function"&&typeof e!="symbol"&&typeof e!="boolean"&&(l.type=e),t!=null||u!=null){if(!(e!=="submit"&&e!=="reset"||t!=null)){rf(l);return}u=u!=null?""+Gl(u):"",t=t!=null?""+Gl(t):u,c||t===l.value||(l.value=t),l.defaultValue=t}a=a??n,a=typeof a!="function"&&typeof a!="symbol"&&!!a,l.checked=c?l.checked:!!a,l.defaultChecked=!!a,f!=null&&typeof f!="function"&&typeof f!="symbol"&&typeof f!="boolean"&&(l.name=f),rf(l)}function Wf(l,t,u){t==="number"&&le(l.ownerDocument)===l||l.defaultValue===""+u||(l.defaultValue=""+u)}function Zu(l,t,u,a){if(l=l.options,t){t={};for(var n=0;n<u.length;n++)t["$"+u[n]]=!0;for(u=0;u<l.length;u++)n=t.hasOwnProperty("$"+l[u].value),l[u].selected!==n&&(l[u].selected=n),n&&a&&(l[u].defaultSelected=!0)}else{for(u=""+Gl(u),t=null,n=0;n<l.length;n++){if(l[n].value===u){l[n].selected=!0,a&&(l[n].defaultSelected=!0);return}t!==null||l[n].disabled||(t=l[n])}t!==null&&(t.selected=!0)}}function F1(l,t,u){if(t!=null&&(t=""+Gl(t),t!==l.value&&(l.value=t),u==null)){l.defaultValue!==t&&(l.defaultValue=t);return}l.defaultValue=u!=null?""+Gl(u):""}function k1(l,t,u,a){if(t==null){if(a!=null){if(u!=null)throw Error(b(92));if(Ta(a)){if(1<a.length)throw Error(b(93));a=a[0]}u=a}u==null&&(u=""),t=u}u=Gl(t),l.defaultValue=u,a=l.textContent,a===u&&a!==""&&a!==null&&(l.value=a),rf(l)}function wu(l,t){if(t){var u=l.firstChild;if(u&&u===l.lastChild&&u.nodeType===3){u.nodeValue=t;return}}l.textContent=t}var bd=new Set("animationIterationCount aspectRatio borderImageOutset borderImageSlice borderImageWidth boxFlex boxFlexGroup boxOrdinalGroup columnCount columns flex flexGrow flexPositive flexShrink flexNegative flexOrder gridArea gridRow gridRowEnd gridRowSpan gridRowStart gridColumn gridColumnEnd gridColumnSpan gridColumnStart fontWeight lineClamp lineHeight opacity order orphans scale tabSize widows zIndex zoom fillOpacity floodOpacity stopOpacity strokeDasharray strokeDashoffset strokeMiterlimit strokeOpacity strokeWidth MozAnimationIterationCount MozBoxFlex MozBoxFlexGroup MozLineClamp msAnimationIterationCount msFlex msZoom msFlexGrow msFlexNegative msFlexOrder msFlexPositive msFlexShrink msGridColumn msGridColumnSpan msGridRow msGridRowSpan WebkitAnimationIterationCount WebkitBoxFlex WebKitBoxFlexGroup WebkitBoxOrdinalGroup WebkitColumnCount WebkitColumns WebkitFlex WebkitFlexGrow WebkitFlexPositive WebkitFlexShrink WebkitLineClamp".split(" "));function h0(l,t,u){var a=t.indexOf("--")===0;u==null||typeof u=="boolean"||u===""?a?l.setProperty(t,""):t==="float"?l.cssFloat="":l[t]="":a?l.setProperty(t,u):typeof u!="number"||u===0||bd.has(t)?t==="float"?l.cssFloat=u:l[t]=(""+u).trim():l[t]=u+"px"}function I1(l,t,u){if(t!=null&&typeof t!="object")throw Error(b(62));if(l=l.style,u!=null){for(var a in u)!u.hasOwnProperty(a)||t!=null&&t.hasOwnProperty(a)||(a.indexOf("--")===0?l.setProperty(a,""):a==="float"?l.cssFloat="":l[a]="");for(var n in t)a=t[n],t.hasOwnProperty(n)&&u[n]!==a&&h0(l,n,a)}else for(var e in t)t.hasOwnProperty(e)&&h0(l,e,t[e])}function Qc(l){if(l.indexOf("-")===-1)return!1;switch(l){case"annotation-xml":case"color-profile":case"font-face":case"font-face-src":case"font-face-uri":case"font-face-format":case"font-face-name":case"missing-glyph":return!1;default:return!0}}var zd=new Map([["acceptCharset","accept-charset"],["htmlFor","for"],["httpEquiv","http-equiv"],["crossOrigin","crossorigin"],["accentHeight","accent-height"],["alignmentBaseline","alignment-baseline"],["arabicForm","arabic-form"],["baselineShift","baseline-shift"],["capHeight","cap-height"],["clipPath","clip-path"],["clipRule","clip-rule"],["colorInterpolation","color-interpolation"],["colorInterpolationFilters","color-interpolation-filters"],["colorProfile","color-profile"],["colorRendering","color-rendering"],["dominantBaseline","dominant-baseline"],["enableBackground","enable-background"],["fillOpacity","fill-opacity"],["fillRule","fill-rule"],["floodColor","flood-color"],["floodOpacity","flood-opacity"],["fontFamily","font-family"],["fontSize","font-size"],["fontSizeAdjust","font-size-adjust"],["fontStretch","font-stretch"],["fontStyle","font-style"],["fontVariant","font-variant"],["fontWeight","font-weight"],["glyphName","glyph-name"],["glyphOrientationHorizontal","glyph-orientation-horizontal"],["glyphOrientationVertical","glyph-orientation-vertical"],["horizAdvX","horiz-adv-x"],["horizOriginX","horiz-origin-x"],["imageRendering","image-rendering"],["letterSpacing","letter-spacing"],["lightingColor","lighting-color"],["markerEnd","marker-end"],["markerMid","marker-mid"],["markerStart","marker-start"],["overlinePosition","overline-position"],["overlineThickness","overline-thickness"],["paintOrder","paint-order"],["panose-1","panose-1"],["pointerEvents","pointer-events"],["renderingIntent","rendering-intent"],["shapeRendering","shape-rendering"],["stopColor","stop-color"],["stopOpacity","stop-opacity"],["strikethroughPosition","strikethrough-position"],["strikethroughThickness","strikethrough-thickness"],["strokeDasharray","stroke-dasharray"],["strokeDashoffset","stroke-dashoffset"],["strokeLinecap","stroke-linecap"],["strokeLinejoin","stroke-linejoin"],["strokeMiterlimit","stroke-miterlimit"],["strokeOpacity","stroke-opacity"],["strokeWidth","stroke-width"],["textAnchor","text-anchor"],["textDecoration","text-decoration"],["textRendering","text-rendering"],["transformOrigin","transform-origin"],["underlinePosition","underline-position"],["underlineThickness","underline-thickness"],["unicodeBidi","unicode-bidi"],["unicodeRange","unicode-range"],["unitsPerEm","units-per-em"],["vAlphabetic","v-alphabetic"],["vHanging","v-hanging"],["vIdeographic","v-ideographic"],["vMathematical","v-mathematical"],["vectorEffect","vector-effect"],["vertAdvY","vert-adv-y"],["vertOriginX","vert-origin-x"],["vertOriginY","vert-origin-y"],["wordSpacing","word-spacing"],["writingMode","writing-mode"],["xmlnsXlink","xmlns:xlink"],["xHeight","x-height"]]),Ed=/^[\u0000-\u001F ]*j[\r\n\t]*a[\r\n\t]*v[\r\n\t]*a[\r\n\t]*s[\r\n\t]*c[\r\n\t]*r[\r\n\t]*i[\r\n\t]*p[\r\n\t]*t[\r\n\t]*:/i;function Gn(l){return Ed.test(""+l)?"javascript:throw new Error('React has blocked a javascript: URL as a security precaution.')":l}function vt(){}var $f=null;function Zc(l){return l=l.target||l.srcElement||window,l.correspondingUseElement&&(l=l.correspondingUseElement),l.nodeType===3?l.parentNode:l}var Nu=null,ju=null;function S0(l){var t=aa(l);if(t&&(l=t.stateNode)){var u=l[Al]||null;l:switch(l=t.stateNode,t.type){case"input":if(wf(l,u.value,u.defaultValue,u.defaultValue,u.checked,u.defaultChecked,u.type,u.name),t=u.name,u.type==="radio"&&t!=null){for(u=l;u.parentNode;)u=u.parentNode;for(u=u.querySelectorAll('input[name="'+Zl(""+t)+'"][type="radio"]'),t=0;t<u.length;t++){var a=u[t];if(a!==l&&a.form===l.form){var n=a[Al]||null;if(!n)throw Error(b(90));wf(a,n.value,n.defaultValue,n.defaultValue,n.checked,n.defaultChecked,n.type,n.name)}}for(t=0;t<u.length;t++)a=u[t],a.form===l.form&&W1(a)}break l;case"textarea":F1(l,u.value,u.defaultValue);break l;case"select":t=u.value,t!=null&&Zu(l,!!u.multiple,t,!1)}}}var yf=!1;function P1(l,t,u){if(yf)return l(t,u);yf=!0;try{var a=l(t);return a}finally{if(yf=!1,(Nu!==null||ju!==null)&&(Xe(),Nu&&(t=Nu,l=ju,ju=Nu=null,S0(t),l)))for(t=0;t<l.length;t++)S0(l[t])}}function Za(l,t){var u=l.stateNode;if(u===null)return null;var a=u[Al]||null;if(a===null)return null;u=a[t];l:switch(t){case"onClick":case"onClickCapture":case"onDoubleClick":case"onDoubleClickCapture":case"onMouseDown":case"onMouseDownCapture":case"onMouseMove":case"onMouseMoveCapture":case"onMouseUp":case"onMouseUpCapture":case"onMouseEnter":(a=!a.disabled)||(l=l.type,a=!(l==="button"||l==="input"||l==="select"||l==="textarea")),l=!a;break l;default:l=!1}if(l)return null;if(u&&typeof u!="function")throw Error(b(231,t,typeof u));return u}var gt=!(typeof window>"u"||typeof window.document>"u"||typeof window.document.createElement>"u"),Ff=!1;if(gt)try{Tu={},Object.defineProperty(Tu,"passive",{get:function(){Ff=!0}}),window.addEventListener("test",Tu,Tu),window.removeEventListener("test",Tu,Tu)}catch{Ff=!1}var Tu,Bt=null,jc=null,Xn=null;function ly(){if(Xn)return Xn;var l,t=jc,u=t.length,a,n="value"in Bt?Bt.value:Bt.textContent,e=n.length;for(l=0;l<u&&t[l]===n[l];l++);var f=u-l;for(a=1;a<=f&&t[u-a]===n[e-a];a++);return Xn=n.slice(l,1<a?1-a:void 0)}function Qn(l){var t=l.keyCode;return"charCode"in l?(l=l.charCode,l===0&&t===13&&(l=13)):l=t,l===10&&(l=13),32<=l||l===13?l:0}function An(){return!0}function g0(){return!1}function Ol(l){function t(u,a,n,e,f){this._reactName=u,this._targetInst=n,this.type=a,this.nativeEvent=e,this.target=f,this.currentTarget=null;for(var c in l)l.hasOwnProperty(c)&&(u=l[c],this[c]=u?u(e):e[c]);return this.isDefaultPrevented=(e.defaultPrevented!=null?e.defaultPrevented:e.returnValue===!1)?An:g0,this.isPropagationStopped=g0,this}return r(t.prototype,{preventDefault:function(){this.defaultPrevented=!0;var u=this.nativeEvent;u&&(u.preventDefault?u.preventDefault():typeof u.returnValue!="unknown"&&(u.returnValue=!1),this.isDefaultPrevented=An)},stopPropagation:function(){var u=this.nativeEvent;u&&(u.stopPropagation?u.stopPropagation():typeof u.cancelBubble!="unknown"&&(u.cancelBubble=!0),this.isPropagationStopped=An)},persist:function(){},isPersistent:An}),t}var hu={eventPhase:0,bubbles:0,cancelable:0,timeStamp:function(l){return l.timeStamp||Date.now()},defaultPrevented:0,isTrusted:0},De=Ol(hu),an=r({},hu,{view:0,detail:0}),Td=Ol(an),vf,mf,Sa,Ue=r({},an,{screenX:0,screenY:0,clientX:0,clientY:0,pageX:0,pageY:0,ctrlKey:0,shiftKey:0,altKey:0,metaKey:0,getModifierState:Vc,button:0,buttons:0,relatedTarget:function(l){return l.relatedTarget===void 0?l.fromElement===l.srcElement?l.toElement:l.fromElement:l.relatedTarget},movementX:function(l){return"movementX"in l?l.movementX:(l!==Sa&&(Sa&&l.type==="mousemove"?(vf=l.screenX-Sa.screenX,mf=l.screenY-Sa.screenY):mf=vf=0,Sa=l),vf)},movementY:function(l){return"movementY"in l?l.movementY:mf}}),o0=Ol(Ue),Ad=r({},Ue,{dataTransfer:0}),Od=Ol(Ad),_d=r({},an,{relatedTarget:0}),df=Ol(_d),Md=r({},hu,{animationName:0,elapsedTime:0,pseudoElement:0}),Dd=Ol(Md),Ud=r({},hu,{clipboardData:function(l){return"clipboardData"in l?l.clipboardData:window.clipboardData}}),Hd=Ol(Ud),Nd=r({},hu,{data:0}),s0=Ol(Nd),pd={Esc:"Escape",Spacebar:" ",Left:"ArrowLeft",Up:"ArrowUp",Right:"ArrowRight",Down:"ArrowDown",Del:"Delete",Win:"OS",Menu:"ContextMenu",Apps:"ContextMenu",Scroll:"ScrollLock",MozPrintableKey:"Unidentified"},qd={8:"Backspace",9:"Tab",12:"Clear",13:"Enter",16:"Shift",17:"Control",18:"Alt",19:"Pause",20:"CapsLock",27:"Escape",32:" ",33:"PageUp",34:"PageDown",35:"End",36:"Home",37:"ArrowLeft",38:"ArrowUp",39:"ArrowRight",40:"ArrowDown",45:"Insert",46:"Delete",112:"F1",113:"F2",114:"F3",115:"F4",116:"F5",117:"F6",118:"F7",119:"F8",120:"F9",121:"F10",122:"F11",123:"F12",144:"NumLock",145:"ScrollLock",224:"Meta"},Bd={Alt:"altKey",Control:"ctrlKey",Meta:"metaKey",Shift:"shiftKey"};function Yd(l){var t=this.nativeEvent;return t.getModifierState?t.getModifierState(l):(l=Bd[l])?!!t[l]:!1}function Vc(){return Yd}var Rd=r({},an,{key:function(l){if(l.key){var t=pd[l.key]||l.key;if(t!=="Unidentified")return t}return l.type==="keypress"?(l=Qn(l),l===13?"Enter":String.fromCharCode(l)):l.type==="keydown"||l.type==="keyup"?qd[l.keyCode]||"Unidentified":""},code:0,location:0,ctrlKey:0,shiftKey:0,altKey:0,metaKey:0,repeat:0,locale:0,getModifierState:Vc,charCode:function(l){return l.type==="keypress"?Qn(l):0},keyCode:function(l){return l.type==="keydown"||l.type==="keyup"?l.keyCode:0},which:function(l){return l.type==="keypress"?Qn(l):l.type==="keydown"||l.type==="keyup"?l.keyCode:0}}),Cd=Ol(Rd),Gd=r({},Ue,{pointerId:0,width:0,height:0,pressure:0,tangentialPressure:0,tiltX:0,tiltY:0,twist:0,pointerType:0,isPrimary:0}),b0=Ol(Gd),Xd=r({},an,{touches:0,targetTouches:0,changedTouches:0,altKey:0,metaKey:0,ctrlKey:0,shiftKey:0,getModifierState:Vc}),Qd=Ol(Xd),Zd=r({},hu,{propertyName:0,elapsedTime:0,pseudoElement:0}),jd=Ol(Zd),Vd=r({},Ue,{deltaX:function(l){return"deltaX"in l?l.deltaX:"wheelDeltaX"in l?-l.wheelDeltaX:0},deltaY:function(l){return"deltaY"in l?l.deltaY:"wheelDeltaY"in l?-l.wheelDeltaY:"wheelDelta"in l?-l.wheelDelta:0},deltaZ:0,deltaMode:0}),xd=Ol(Vd),Ld=r({},hu,{newState:0,oldState:0}),Kd=Ol(Ld),Jd=[9,13,27,32],xc=gt&&"CompositionEvent"in window,Ma=null;gt&&"documentMode"in document&&(Ma=document.documentMode);var rd=gt&&"TextEvent"in window&&!Ma,ty=gt&&(!xc||Ma&&8<Ma&&11>=Ma),z0=" ",E0=!1;function uy(l,t){switch(l){case"keyup":return Jd.indexOf(t.keyCode)!==-1;case"keydown":return t.keyCode!==229;case"keypress":case"mousedown":case"focusout":return!0;default:return!1}}function ay(l){return l=l.detail,typeof l=="object"&&"data"in l?l.data:null}var pu=!1;function wd(l,t){switch(l){case"compositionend":return ay(t);case"keypress":return t.which!==32?null:(E0=!0,z0);case"textInput":return l=t.data,l===z0&&E0?null:l;default:return null}}function Wd(l,t){if(pu)return l==="compositionend"||!xc&&uy(l,t)?(l=ly(),Xn=jc=Bt=null,pu=!1,l):null;switch(l){case"paste":return null;case"keypress":if(!(t.ctrlKey||t.altKey||t.metaKey)||t.ctrlKey&&t.altKey){if(t.char&&1<t.char.length)return t.char;if(t.which)return String.fromCharCode(t.which)}return null;case"compositionend":return ty&&t.locale!=="ko"?null:t.data;default:return null}}var $d={color:!0,date:!0,datetime:!0,"datetime-local":!0,email:!0,month:!0,number:!0,password:!0,range:!0,search:!0,tel:!0,text:!0,time:!0,url:!0,week:!0};function T0(l){var t=l&&l.nodeName&&l.nodeName.toLowerCase();return t==="input"?!!$d[l.type]:t==="textarea"}function ny(l,t,u,a){Nu?ju?ju.push(a):ju=[a]:Nu=a,t=be(t,"onChange"),0<t.length&&(u=new De("onChange","change",null,u,a),l.push({event:u,listeners:t}))}var Da=null,ja=null;function Fd(l){Pv(l,0)}function He(l){var t=Aa(l);if(W1(t))return l}function A0(l,t){if(l==="change")return t}var ey=!1;gt&&(gt?(_n="oninput"in document,_n||(hf=document.createElement("div"),hf.setAttribute("oninput","return;"),_n=typeof hf.oninput=="function"),On=_n):On=!1,ey=On&&(!document.documentMode||9<document.documentMode));var On,_n,hf;function O0(){Da&&(Da.detachEvent("onpropertychange",fy),ja=Da=null)}function fy(l){if(l.propertyName==="value"&&He(ja)){var t=[];ny(t,ja,l,Zc(l)),P1(Fd,t)}}function kd(l,t,u){l==="focusin"?(O0(),Da=t,ja=u,Da.attachEvent("onpropertychange",fy)):l==="focusout"&&O0()}function Id(l){if(l==="selectionchange"||l==="keyup"||l==="keydown")return He(ja)}function Pd(l,t){if(l==="click")return He(t)}function lh(l,t){if(l==="input"||l==="change")return He(t)}function th(l,t){return l===t&&(l!==0||1/l===1/t)||l!==l&&t!==t}var Bl=typeof Object.is=="function"?Object.is:th;function Va(l,t){if(Bl(l,t))return!0;if(typeof l!="object"||l===null||typeof t!="object"||t===null)return!1;var u=Object.keys(l),a=Object.keys(t);if(u.length!==a.length)return!1;for(a=0;a<u.length;a++){var n=u[a];if(!Kf.call(t,n)||!Bl(l[n],t[n]))return!1}return!0}function _0(l){for(;l&&l.firstChild;)l=l.firstChild;return l}function M0(l,t){var u=_0(l);l=0;for(var a;u;){if(u.nodeType===3){if(a=l+u.textContent.length,l<=t&&a>=t)return{node:u,offset:t-l};l=a}l:{for(;u;){if(u.nextSibling){u=u.nextSibling;break l}u=u.parentNode}u=void 0}u=_0(u)}}function cy(l,t){return l&&t?l===t?!0:l&&l.nodeType===3?!1:t&&t.nodeType===3?cy(l,t.parentNode):"contains"in l?l.contains(t):l.compareDocumentPosition?!!(l.compareDocumentPosition(t)&16):!1:!1}function iy(l){l=l!=null&&l.ownerDocument!=null&&l.ownerDocument.defaultView!=null?l.ownerDocument.defaultView:window;for(var t=le(l.document);t instanceof l.HTMLIFrameElement;){try{var u=typeof t.contentWindow.location.href=="string"}catch{u=!1}if(u)l=t.contentWindow;else break;t=le(l.document)}return t}function Lc(l){var t=l&&l.nodeName&&l.nodeName.toLowerCase();return t&&(t==="input"&&(l.type==="text"||l.type==="search"||l.type==="tel"||l.type==="url"||l.type==="password")||t==="textarea"||l.contentEditable==="true")}var uh=gt&&"documentMode"in document&&11>=document.documentMode,qu=null,kf=null,Ua=null,If=!1;function D0(l,t,u){var a=u.window===u?u.document:u.nodeType===9?u:u.ownerDocument;If||qu==null||qu!==le(a)||(a=qu,"selectionStart"in a&&Lc(a)?a={start:a.selectionStart,end:a.selectionEnd}:(a=(a.ownerDocument&&a.ownerDocument.defaultView||window).getSelection(),a={anchorNode:a.anchorNode,anchorOffset:a.anchorOffset,focusNode:a.focusNode,focusOffset:a.focusOffset}),Ua&&Va(Ua,a)||(Ua=a,a=be(kf,"onSelect"),0<a.length&&(t=new De("onSelect","select",null,t,u),l.push({event:t,listeners:a}),t.target=qu)))}function kt(l,t){var u={};return u[l.toLowerCase()]=t.toLowerCase(),u["Webkit"+l]="webkit"+t,u["Moz"+l]="moz"+t,u}var Bu={animationend:kt("Animation","AnimationEnd"),animationiteration:kt("Animation","AnimationIteration"),animationstart:kt("Animation","AnimationStart"),transitionrun:kt("Transition","TransitionRun"),transitionstart:kt("Transition","TransitionStart"),transitioncancel:kt("Transition","TransitionCancel"),transitionend:kt("Transition","TransitionEnd")},Sf={},yy={};gt&&(yy=document.createElement("div").style,"AnimationEvent"in window||(delete Bu.animationend.animation,delete Bu.animationiteration.animation,delete Bu.animationstart.animation),"TransitionEvent"in window||delete Bu.transitionend.transition);function Su(l){if(Sf[l])return Sf[l];if(!Bu[l])return l;var t=Bu[l],u;for(u in t)if(t.hasOwnProperty(u)&&u in yy)return Sf[l]=t[u];return l}var vy=Su("animationend"),my=Su("animationiteration"),dy=Su("animationstart"),ah=Su("transitionrun"),nh=Su("transitionstart"),eh=Su("transitioncancel"),hy=Su("transitionend"),Sy=new Map,Pf="abort auxClick beforeToggle cancel canPlay canPlayThrough click close contextMenu copy cut drag dragEnd dragEnter dragExit dragLeave dragOver dragStart drop durationChange emptied encrypted ended error gotPointerCapture input invalid keyDown keyPress keyUp load loadedData loadedMetadata loadStart lostPointerCapture mouseDown mouseMove mouseOut mouseOver mouseUp paste pause play playing pointerCancel pointerDown pointerMove pointerOut pointerOver pointerUp progress rateChange reset resize seeked seeking stalled submit suspend timeUpdate touchCancel touchEnd touchStart volumeChange scroll toggle touchMove waiting wheel".split(" ");Pf.push("scrollEnd");function wl(l,t){Sy.set(l,t),du(t,[l])}var te=typeof reportError=="function"?reportError:function(l){if(typeof window=="object"&&typeof window.ErrorEvent=="function"){var t=new window.ErrorEvent("error",{bubbles:!0,cancelable:!0,message:typeof l=="object"&&l!==null&&typeof l.message=="string"?String(l.message):String(l),error:l});if(!window.dispatchEvent(t))return}else if(typeof process=="object"&&typeof process.emit=="function"){process.emit("uncaughtException",l);return}console.error(l)},Cl=[],Yu=0,Kc=0;function Ne(){for(var l=Yu,t=Kc=Yu=0;t<l;){var u=Cl[t];Cl[t++]=null;var a=Cl[t];Cl[t++]=null;var n=Cl[t];Cl[t++]=null;var e=Cl[t];if(Cl[t++]=null,a!==null&&n!==null){var f=a.pending;f===null?n.next=n:(n.next=f.next,f.next=n),a.pending=n}e!==0&&gy(u,n,e)}}function pe(l,t,u,a){Cl[Yu++]=l,Cl[Yu++]=t,Cl[Yu++]=u,Cl[Yu++]=a,Kc|=a,l.lanes|=a,l=l.alternate,l!==null&&(l.lanes|=a)}function Jc(l,t,u,a){return pe(l,t,u,a),ue(l)}function gu(l,t){return pe(l,null,null,t),ue(l)}function gy(l,t,u){l.lanes|=u;var a=l.alternate;a!==null&&(a.lanes|=u);for(var n=!1,e=l.return;e!==null;)e.childLanes|=u,a=e.alternate,a!==null&&(a.childLanes|=u),e.tag===22&&(l=e.stateNode,l===null||l._visibility&1||(n=!0)),l=e,e=e.return;return l.tag===3?(e=l.stateNode,n&&t!==null&&(n=31-pl(u),l=e.hiddenUpdates,a=l[n],a===null?l[n]=[t]:a.push(t),t.lane=u|536870912),e):null}function ue(l){if(50<Ga)throw Ga=0,Ec=null,Error(b(185));for(var t=l.return;t!==null;)l=t,t=l.return;return l.tag===3?l.stateNode:null}var Ru={};function fh(l,t,u,a){this.tag=l,this.key=u,this.sibling=this.child=this.return=this.stateNode=this.type=this.elementType=null,this.index=0,this.refCleanup=this.ref=null,this.pendingProps=t,this.dependencies=this.memoizedState=this.updateQueue=this.memoizedProps=null,this.mode=a,this.subtreeFlags=this.flags=0,this.deletions=null,this.childLanes=this.lanes=0,this.alternate=null}function Dl(l,t,u,a){return new fh(l,t,u,a)}function rc(l){return l=l.prototype,!(!l||!l.isReactComponent)}function dt(l,t){var u=l.alternate;return u===null?(u=Dl(l.tag,t,l.key,l.mode),u.elementType=l.elementType,u.type=l.type,u.stateNode=l.stateNode,u.alternate=l,l.alternate=u):(u.pendingProps=t,u.type=l.type,u.flags=0,u.subtreeFlags=0,u.deletions=null),u.flags=l.flags&65011712,u.childLanes=l.childLanes,u.lanes=l.lanes,u.child=l.child,u.memoizedProps=l.memoizedProps,u.memoizedState=l.memoizedState,u.updateQueue=l.updateQueue,t=l.dependencies,u.dependencies=t===null?null:{lanes:t.lanes,firstContext:t.firstContext},u.sibling=l.sibling,u.index=l.index,u.ref=l.ref,u.refCleanup=l.refCleanup,u}function oy(l,t){l.flags&=65011714;var u=l.alternate;return u===null?(l.childLanes=0,l.lanes=t,l.child=null,l.subtreeFlags=0,l.memoizedProps=null,l.memoizedState=null,l.updateQueue=null,l.dependencies=null,l.stateNode=null):(l.childLanes=u.childLanes,l.lanes=u.lanes,l.child=u.child,l.subtreeFlags=0,l.deletions=null,l.memoizedProps=u.memoizedProps,l.memoizedState=u.memoizedState,l.updateQueue=u.updateQueue,l.type=u.type,t=u.dependencies,l.dependencies=t===null?null:{lanes:t.lanes,firstContext:t.firstContext}),l}function Zn(l,t,u,a,n,e){var f=0;if(a=l,typeof l=="function")rc(l)&&(f=1);else if(typeof l=="string")f=y2(l,u,Il.current)?26:l==="html"||l==="head"||l==="body"?27:5;else l:switch(l){case jf:return l=Dl(31,u,t,n),l.elementType=jf,l.lanes=e,l;case Du:return au(u.children,n,e,t);case C1:f=8,n|=24;break;case Xf:return l=Dl(12,u,t,n|2),l.elementType=Xf,l.lanes=e,l;case Qf:return l=Dl(13,u,t,n),l.elementType=Qf,l.lanes=e,l;case Zf:return l=Dl(19,u,t,n),l.elementType=Zf,l.lanes=e,l;default:if(typeof l=="object"&&l!==null)switch(l.$$typeof){case yt:f=10;break l;case G1:f=9;break l;case Bc:f=11;break l;case Yc:f=14;break l;case Mt:f=16,a=null;break l}f=29,u=Error(b(130,l===null?"null":typeof l,"")),a=null}return t=Dl(f,u,t,n),t.elementType=l,t.type=a,t.lanes=e,t}function au(l,t,u,a){return l=Dl(7,l,a,t),l.lanes=u,l}function gf(l,t,u){return l=Dl(6,l,null,t),l.lanes=u,l}function sy(l){var t=Dl(18,null,null,0);return t.stateNode=l,t}function of(l,t,u){return t=Dl(4,l.children!==null?l.children:[],l.key,t),t.lanes=u,t.stateNode={containerInfo:l.containerInfo,pendingChildren:null,implementation:l.implementation},t}var U0=new WeakMap;function jl(l,t){if(typeof l=="object"&&l!==null){var u=U0.get(l);return u!==void 0?u:(t={value:l,source:t,stack:i0(t)},U0.set(l,t),t)}return{value:l,source:t,stack:i0(t)}}var Cu=[],Gu=0,ae=null,xa=0,Xl=[],Ql=0,Jt=null,$l=1,Fl="";function ct(l,t){Cu[Gu++]=xa,Cu[Gu++]=ae,ae=l,xa=t}function by(l,t,u){Xl[Ql++]=$l,Xl[Ql++]=Fl,Xl[Ql++]=Jt,Jt=l;var a=$l;l=Fl;var n=32-pl(a)-1;a&=~(1<<n),u+=1;var e=32-pl(t)+n;if(30<e){var f=n-n%5;e=(a&(1<<f)-1).toString(32),a>>=f,n-=f,$l=1<<32-pl(t)+n|u<<n|a,Fl=e+l}else $l=1<<e|u<<n|a,Fl=l}function wc(l){l.return!==null&&(ct(l,1),by(l,1,0))}function Wc(l){for(;l===ae;)ae=Cu[--Gu],Cu[Gu]=null,xa=Cu[--Gu],Cu[Gu]=null;for(;l===Jt;)Jt=Xl[--Ql],Xl[Ql]=null,Fl=Xl[--Ql],Xl[Ql]=null,$l=Xl[--Ql],Xl[Ql]=null}function zy(l,t){Xl[Ql++]=$l,Xl[Ql++]=Fl,Xl[Ql++]=Jt,$l=t.id,Fl=t.overflow,Jt=l}var vl=null,J=null,q=!1,Xt=null,Vl=!1,lc=Error(b(519));function rt(l){var t=Error(b(418,1<arguments.length&&arguments[1]!==void 0&&arguments[1]?"text":"HTML",""));throw La(jl(t,l)),lc}function H0(l){var t=l.stateNode,u=l.type,a=l.memoizedProps;switch(t[yl]=l,t[Al]=a,u){case"dialog":U("cancel",t),U("close",t);break;case"iframe":case"object":case"embed":U("load",t);break;case"video":case"audio":for(u=0;u<wa.length;u++)U(wa[u],t);break;case"source":U("error",t);break;case"img":case"image":case"link":U("error",t),U("load",t);break;case"details":U("toggle",t);break;case"input":U("invalid",t),$1(t,a.value,a.defaultValue,a.checked,a.defaultChecked,a.type,a.name,!0);break;case"select":U("invalid",t);break;case"textarea":U("invalid",t),k1(t,a.value,a.defaultValue,a.children)}u=a.children,typeof u!="string"&&typeof u!="number"&&typeof u!="bigint"||t.textContent===""+u||a.suppressHydrationWarning===!0||tm(t.textContent,u)?(a.popover!=null&&(U("beforetoggle",t),U("toggle",t)),a.onScroll!=null&&U("scroll",t),a.onScrollEnd!=null&&U("scrollend",t),a.onClick!=null&&(t.onclick=vt),t=!0):t=!1,t||rt(l,!0)}function N0(l){for(vl=l.return;vl;)switch(vl.tag){case 5:case 31:case 13:Vl=!1;return;case 27:case 3:Vl=!0;return;default:vl=vl.return}}function Au(l){if(l!==vl)return!1;if(!q)return N0(l),q=!0,!1;var t=l.tag,u;if((u=t!==3&&t!==27)&&((u=t===5)&&(u=l.type,u=!(u!=="form"&&u!=="button")||Mc(l.type,l.memoizedProps)),u=!u),u&&J&&rt(l),N0(l),t===13){if(l=l.memoizedState,l=l!==null?l.dehydrated:null,!l)throw Error(b(317));J=s1(l)}else if(t===31){if(l=l.memoizedState,l=l!==null?l.dehydrated:null,!l)throw Error(b(317));J=s1(l)}else t===27?(t=J,Ft(l.type)?(l=Nc,Nc=null,J=l):J=t):J=vl?Ll(l.stateNode.nextSibling):null;return!0}function cu(){J=vl=null,q=!1}function sf(){var l=Xt;return l!==null&&(El===null?El=l:El.push.apply(El,l),Xt=null),l}function La(l){Xt===null?Xt=[l]:Xt.push(l)}var tc=Pl(null),ou=null,mt=null;function Ut(l,t,u){x(tc,t._currentValue),t._currentValue=u}function ht(l){l._currentValue=tc.current,cl(tc)}function uc(l,t,u){for(;l!==null;){var a=l.alternate;if((l.childLanes&t)!==t?(l.childLanes|=t,a!==null&&(a.childLanes|=t)):a!==null&&(a.childLanes&t)!==t&&(a.childLanes|=t),l===u)break;l=l.return}}function ac(l,t,u,a){var n=l.child;for(n!==null&&(n.return=l);n!==null;){var e=n.dependencies;if(e!==null){var f=n.child;e=e.firstContext;l:for(;e!==null;){var c=e;e=n;for(var i=0;i<t.length;i++)if(c.context===t[i]){e.lanes|=u,c=e.alternate,c!==null&&(c.lanes|=u),uc(e.return,u,l),a||(f=null);break l}e=c.next}}else if(n.tag===18){if(f=n.return,f===null)throw Error(b(341));f.lanes|=u,e=f.alternate,e!==null&&(e.lanes|=u),uc(f,u,l),f=null}else f=n.child;if(f!==null)f.return=n;else for(f=n;f!==null;){if(f===l){f=null;break}if(n=f.sibling,n!==null){n.return=f.return,f=n;break}f=f.return}n=f}}function na(l,t,u,a){l=null;for(var n=t,e=!1;n!==null;){if(!e){if((n.flags&524288)!==0)e=!0;else if((n.flags&262144)!==0)break}if(n.tag===10){var f=n.alternate;if(f===null)throw Error(b(387));if(f=f.memoizedProps,f!==null){var c=n.type;Bl(n.pendingProps.value,f.value)||(l!==null?l.push(c):l=[c])}}else if(n===Fn.current){if(f=n.alternate,f===null)throw Error(b(387));f.memoizedState.memoizedState!==n.memoizedState.memoizedState&&(l!==null?l.push($a):l=[$a])}n=n.return}l!==null&&ac(t,l,u,a),t.flags|=262144}function ne(l){for(l=l.firstContext;l!==null;){if(!Bl(l.context._currentValue,l.memoizedValue))return!0;l=l.next}return!1}function iu(l){ou=l,mt=null,l=l.dependencies,l!==null&&(l.firstContext=null)}function ml(l){return Ey(ou,l)}function Mn(l,t){return ou===null&&iu(l),Ey(l,t)}function Ey(l,t){var u=t._currentValue;if(t={context:t,memoizedValue:u,next:null},mt===null){if(l===null)throw Error(b(308));mt=t,l.dependencies={lanes:0,firstContext:t},l.flags|=524288}else mt=mt.next=t;return u}var ch=typeof AbortController<"u"?AbortController:function(){var l=[],t=this.signal={aborted:!1,addEventListener:function(u,a){l.push(a)}};this.abort=function(){t.aborted=!0,l.forEach(function(u){return u()})}},ih=nl.unstable_scheduleCallback,yh=nl.unstable_NormalPriority,tl={$$typeof:yt,Consumer:null,Provider:null,_currentValue:null,_currentValue2:null,_threadCount:0};function $c(){return{controller:new ch,data:new Map,refCount:0}}function nn(l){l.refCount--,l.refCount===0&&ih(yh,function(){l.controller.abort()})}var Ha=null,nc=0,Wu=0,Vu=null;function vh(l,t){if(Ha===null){var u=Ha=[];nc=0,Wu=Ei(),Vu={status:"pending",value:void 0,then:function(a){u.push(a)}}}return nc++,t.then(p0,p0),t}function p0(){if(--nc===0&&Ha!==null){Vu!==null&&(Vu.status="fulfilled");var l=Ha;Ha=null,Wu=0,Vu=null;for(var t=0;t<l.length;t++)(0,l[t])()}}function mh(l,t){var u=[],a={status:"pending",value:null,reason:null,then:function(n){u.push(n)}};return l.then(function(){a.status="fulfilled",a.value=t;for(var n=0;n<u.length;n++)(0,u[n])(t)},function(n){for(a.status="rejected",a.reason=n,n=0;n<u.length;n++)(0,u[n])(void 0)}),a}var q0=O.S;O.S=function(l,t){Rv=Hl(),typeof t=="object"&&t!==null&&typeof t.then=="function"&&vh(l,t),q0!==null&&q0(l,t)};var nu=Pl(null);function Fc(){var l=nu.current;return l!==null?l:V.pooledCache}function jn(l,t){t===null?x(nu,nu.current):x(nu,t.pool)}function Ty(){var l=Fc();return l===null?null:{parent:tl._currentValue,pool:l}}var ea=Error(b(460)),kc=Error(b(474)),qe=Error(b(542)),ee={then:function(){}};function B0(l){return l=l.status,l==="fulfilled"||l==="rejected"}function Ay(l,t,u){switch(u=l[u],u===void 0?l.push(t):u!==t&&(t.then(vt,vt),t=u),t.status){case"fulfilled":return t.value;case"rejected":throw l=t.reason,R0(l),l;default:if(typeof t.status=="string")t.then(vt,vt);else{if(l=V,l!==null&&100<l.shellSuspendCounter)throw Error(b(482));l=t,l.status="pending",l.then(function(a){if(t.status==="pending"){var n=t;n.status="fulfilled",n.value=a}},function(a){if(t.status==="pending"){var n=t;n.status="rejected",n.reason=a}})}switch(t.status){case"fulfilled":return t.value;case"rejected":throw l=t.reason,R0(l),l}throw eu=t,ea}}function lu(l){try{var t=l._init;return t(l._payload)}catch(u){throw u!==null&&typeof u=="object"&&typeof u.then=="function"?(eu=u,ea):u}}var eu=null;function Y0(){if(eu===null)throw Error(b(459));var l=eu;return eu=null,l}function R0(l){if(l===ea||l===qe)throw Error(b(483))}var xu=null,Ka=0;function Dn(l){var t=Ka;return Ka+=1,xu===null&&(xu=[]),Ay(xu,l,t)}function ga(l,t){t=t.props.ref,l.ref=t!==void 0?t:null}function Un(l,t){throw t.$$typeof===km?Error(b(525)):(l=Object.prototype.toString.call(t),Error(b(31,l==="[object Object]"?"object with keys {"+Object.keys(t).join(", ")+"}":l)))}function Oy(l){function t(v,y){if(l){var d=v.deletions;d===null?(v.deletions=[y],v.flags|=16):d.push(y)}}function u(v,y){if(!l)return null;for(;y!==null;)t(v,y),y=y.sibling;return null}function a(v){for(var y=new Map;v!==null;)v.key!==null?y.set(v.key,v):y.set(v.index,v),v=v.sibling;return y}function n(v,y){return v=dt(v,y),v.index=0,v.sibling=null,v}function e(v,y,d){return v.index=d,l?(d=v.alternate,d!==null?(d=d.index,d<y?(v.flags|=67108866,y):d):(v.flags|=67108866,y)):(v.flags|=1048576,y)}function f(v){return l&&v.alternate===null&&(v.flags|=67108866),v}function c(v,y,d,o){return y===null||y.tag!==6?(y=gf(d,v.mode,o),y.return=v,y):(y=n(y,d),y.return=v,y)}function i(v,y,d,o){var T=d.type;return T===Du?g(v,y,d.props.children,o,d.key):y!==null&&(y.elementType===T||typeof T=="object"&&T!==null&&T.$$typeof===Mt&&lu(T)===y.type)?(y=n(y,d.props),ga(y,d),y.return=v,y):(y=Zn(d.type,d.key,d.props,null,v.mode,o),ga(y,d),y.return=v,y)}function m(v,y,d,o){return y===null||y.tag!==4||y.stateNode.containerInfo!==d.containerInfo||y.stateNode.implementation!==d.implementation?(y=of(d,v.mode,o),y.return=v,y):(y=n(y,d.children||[]),y.return=v,y)}function g(v,y,d,o,T){return y===null||y.tag!==7?(y=au(d,v.mode,o,T),y.return=v,y):(y=n(y,d),y.return=v,y)}function s(v,y,d){if(typeof y=="string"&&y!==""||typeof y=="number"||typeof y=="bigint")return y=gf(""+y,v.mode,d),y.return=v,y;if(typeof y=="object"&&y!==null){switch(y.$$typeof){case sn:return d=Zn(y.type,y.key,y.props,null,v.mode,d),ga(d,y),d.return=v,d;case Ea:return y=of(y,v.mode,d),y.return=v,y;case Mt:return y=lu(y),s(v,y,d)}if(Ta(y)||ha(y))return y=au(y,v.mode,d,null),y.return=v,y;if(typeof y.then=="function")return s(v,Dn(y),d);if(y.$$typeof===yt)return s(v,Mn(v,y),d);Un(v,y)}return null}function h(v,y,d,o){var T=y!==null?y.key:null;if(typeof d=="string"&&d!==""||typeof d=="number"||typeof d=="bigint")return T!==null?null:c(v,y,""+d,o);if(typeof d=="object"&&d!==null){switch(d.$$typeof){case sn:return d.key===T?i(v,y,d,o):null;case Ea:return d.key===T?m(v,y,d,o):null;case Mt:return d=lu(d),h(v,y,d,o)}if(Ta(d)||ha(d))return T!==null?null:g(v,y,d,o,null);if(typeof d.then=="function")return h(v,y,Dn(d),o);if(d.$$typeof===yt)return h(v,y,Mn(v,d),o);Un(v,d)}return null}function S(v,y,d,o,T){if(typeof o=="string"&&o!==""||typeof o=="number"||typeof o=="bigint")return v=v.get(d)||null,c(y,v,""+o,T);if(typeof o=="object"&&o!==null){switch(o.$$typeof){case sn:return v=v.get(o.key===null?d:o.key)||null,i(y,v,o,T);case Ea:return v=v.get(o.key===null?d:o.key)||null,m(y,v,o,T);case Mt:return o=lu(o),S(v,y,d,o,T)}if(Ta(o)||ha(o))return v=v.get(d)||null,g(y,v,o,T,null);if(typeof o.then=="function")return S(v,y,d,Dn(o),T);if(o.$$typeof===yt)return S(v,y,d,Mn(y,o),T);Un(y,o)}return null}function z(v,y,d,o){for(var T=null,B=null,E=y,D=y=0,N=null;E!==null&&D<d.length;D++){E.index>D?(N=E,E=null):N=E.sibling;var Y=h(v,E,d[D],o);if(Y===null){E===null&&(E=N);break}l&&E&&Y.alternate===null&&t(v,E),y=e(Y,y,D),B===null?T=Y:B.sibling=Y,B=Y,E=N}if(D===d.length)return u(v,E),q&&ct(v,D),T;if(E===null){for(;D<d.length;D++)E=s(v,d[D],o),E!==null&&(y=e(E,y,D),B===null?T=E:B.sibling=E,B=E);return q&&ct(v,D),T}for(E=a(E);D<d.length;D++)N=S(E,v,D,d[D],o),N!==null&&(l&&N.alternate!==null&&E.delete(N.key===null?D:N.key),y=e(N,y,D),B===null?T=N:B.sibling=N,B=N);return l&&E.forEach(function(Tt){return t(v,Tt)}),q&&ct(v,D),T}function A(v,y,d,o){if(d==null)throw Error(b(151));for(var T=null,B=null,E=y,D=y=0,N=null,Y=d.next();E!==null&&!Y.done;D++,Y=d.next()){E.index>D?(N=E,E=null):N=E.sibling;var Tt=h(v,E,Y.value,o);if(Tt===null){E===null&&(E=N);break}l&&E&&Tt.alternate===null&&t(v,E),y=e(Tt,y,D),B===null?T=Tt:B.sibling=Tt,B=Tt,E=N}if(Y.done)return u(v,E),q&&ct(v,D),T;if(E===null){for(;!Y.done;D++,Y=d.next())Y=s(v,Y.value,o),Y!==null&&(y=e(Y,y,D),B===null?T=Y:B.sibling=Y,B=Y);return q&&ct(v,D),T}for(E=a(E);!Y.done;D++,Y=d.next())Y=S(E,v,D,Y.value,o),Y!==null&&(l&&Y.alternate!==null&&E.delete(Y.key===null?D:Y.key),y=e(Y,y,D),B===null?T=Y:B.sibling=Y,B=Y);return l&&E.forEach(function(Am){return t(v,Am)}),q&&ct(v,D),T}function Q(v,y,d,o){if(typeof d=="object"&&d!==null&&d.type===Du&&d.key===null&&(d=d.props.children),typeof d=="object"&&d!==null){switch(d.$$typeof){case sn:l:{for(var T=d.key;y!==null;){if(y.key===T){if(T=d.type,T===Du){if(y.tag===7){u(v,y.sibling),o=n(y,d.props.children),o.return=v,v=o;break l}}else if(y.elementType===T||typeof T=="object"&&T!==null&&T.$$typeof===Mt&&lu(T)===y.type){u(v,y.sibling),o=n(y,d.props),ga(o,d),o.return=v,v=o;break l}u(v,y);break}else t(v,y);y=y.sibling}d.type===Du?(o=au(d.props.children,v.mode,o,d.key),o.return=v,v=o):(o=Zn(d.type,d.key,d.props,null,v.mode,o),ga(o,d),o.return=v,v=o)}return f(v);case Ea:l:{for(T=d.key;y!==null;){if(y.key===T)if(y.tag===4&&y.stateNode.containerInfo===d.containerInfo&&y.stateNode.implementation===d.implementation){u(v,y.sibling),o=n(y,d.children||[]),o.return=v,v=o;break l}else{u(v,y);break}else t(v,y);y=y.sibling}o=of(d,v.mode,o),o.return=v,v=o}return f(v);case Mt:return d=lu(d),Q(v,y,d,o)}if(Ta(d))return z(v,y,d,o);if(ha(d)){if(T=ha(d),typeof T!="function")throw Error(b(150));return d=T.call(d),A(v,y,d,o)}if(typeof d.then=="function")return Q(v,y,Dn(d),o);if(d.$$typeof===yt)return Q(v,y,Mn(v,d),o);Un(v,d)}return typeof d=="string"&&d!==""||typeof d=="number"||typeof d=="bigint"?(d=""+d,y!==null&&y.tag===6?(u(v,y.sibling),o=n(y,d),o.return=v,v=o):(u(v,y),o=gf(d,v.mode,o),o.return=v,v=o),f(v)):u(v,y)}return function(v,y,d,o){try{Ka=0;var T=Q(v,y,d,o);return xu=null,T}catch(E){if(E===ea||E===qe)throw E;var B=Dl(29,E,null,v.mode);return B.lanes=o,B.return=v,B}}}var yu=Oy(!0),_y=Oy(!1),Dt=!1;function Ic(l){l.updateQueue={baseState:l.memoizedState,firstBaseUpdate:null,lastBaseUpdate:null,shared:{pending:null,lanes:0,hiddenCallbacks:null},callbacks:null}}function ec(l,t){l=l.updateQueue,t.updateQueue===l&&(t.updateQueue={baseState:l.baseState,firstBaseUpdate:l.firstBaseUpdate,lastBaseUpdate:l.lastBaseUpdate,shared:l.shared,callbacks:null})}function Qt(l){return{lane:l,tag:0,payload:null,callback:null,next:null}}function Zt(l,t,u){var a=l.updateQueue;if(a===null)return null;if(a=a.shared,(R&2)!==0){var n=a.pending;return n===null?t.next=t:(t.next=n.next,n.next=t),a.pending=t,t=ue(l),gy(l,null,u),t}return pe(l,a,t,u),ue(l)}function Na(l,t,u){if(t=t.updateQueue,t!==null&&(t=t.shared,(u&4194048)!==0)){var a=t.lanes;a&=l.pendingLanes,u|=a,t.lanes=u,x1(l,u)}}function bf(l,t){var u=l.updateQueue,a=l.alternate;if(a!==null&&(a=a.updateQueue,u===a)){var n=null,e=null;if(u=u.firstBaseUpdate,u!==null){do{var f={lane:u.lane,tag:u.tag,payload:u.payload,callback:null,next:null};e===null?n=e=f:e=e.next=f,u=u.next}while(u!==null);e===null?n=e=t:e=e.next=t}else n=e=t;u={baseState:a.baseState,firstBaseUpdate:n,lastBaseUpdate:e,shared:a.shared,callbacks:a.callbacks},l.updateQueue=u;return}l=u.lastBaseUpdate,l===null?u.firstBaseUpdate=t:l.next=t,u.lastBaseUpdate=t}var fc=!1;function pa(){if(fc){var l=Vu;if(l!==null)throw l}}function qa(l,t,u,a){fc=!1;var n=l.updateQueue;Dt=!1;var e=n.firstBaseUpdate,f=n.lastBaseUpdate,c=n.shared.pending;if(c!==null){n.shared.pending=null;var i=c,m=i.next;i.next=null,f===null?e=m:f.next=m,f=i;var g=l.alternate;g!==null&&(g=g.updateQueue,c=g.lastBaseUpdate,c!==f&&(c===null?g.firstBaseUpdate=m:c.next=m,g.lastBaseUpdate=i))}if(e!==null){var s=n.baseState;f=0,g=m=i=null,c=e;do{var h=c.lane&-536870913,S=h!==c.lane;if(S?(p&h)===h:(a&h)===h){h!==0&&h===Wu&&(fc=!0),g!==null&&(g=g.next={lane:0,tag:c.tag,payload:c.payload,callback:null,next:null});l:{var z=l,A=c;h=t;var Q=u;switch(A.tag){case 1:if(z=A.payload,typeof z=="function"){s=z.call(Q,s,h);break l}s=z;break l;case 3:z.flags=z.flags&-65537|128;case 0:if(z=A.payload,h=typeof z=="function"?z.call(Q,s,h):z,h==null)break l;s=r({},s,h);break l;case 2:Dt=!0}}h=c.callback,h!==null&&(l.flags|=64,S&&(l.flags|=8192),S=n.callbacks,S===null?n.callbacks=[h]:S.push(h))}else S={lane:h,tag:c.tag,payload:c.payload,callback:c.callback,next:null},g===null?(m=g=S,i=s):g=g.next=S,f|=h;if(c=c.next,c===null){if(c=n.shared.pending,c===null)break;S=c,c=S.next,S.next=null,n.lastBaseUpdate=S,n.shared.pending=null}}while(!0);g===null&&(i=s),n.baseState=i,n.firstBaseUpdate=m,n.lastBaseUpdate=g,e===null&&(n.shared.lanes=0),Wt|=f,l.lanes=f,l.memoizedState=s}}function My(l,t){if(typeof l!="function")throw Error(b(191,l));l.call(t)}function Dy(l,t){var u=l.callbacks;if(u!==null)for(l.callbacks=null,l=0;l<u.length;l++)My(u[l],t)}var $u=Pl(null),fe=Pl(0);function C0(l,t){l=zt,x(fe,l),x($u,t),zt=l|t.baseLanes}function cc(){x(fe,zt),x($u,$u.current)}function Pc(){zt=fe.current,cl($u),cl(fe)}var Yl=Pl(null),xl=null;function Ht(l){var t=l.alternate;x(k,k.current&1),x(Yl,l),xl===null&&(t===null||$u.current!==null||t.memoizedState!==null)&&(xl=l)}function ic(l){x(k,k.current),x(Yl,l),xl===null&&(xl=l)}function Uy(l){l.tag===22?(x(k,k.current),x(Yl,l),xl===null&&(xl=l)):Nt(l)}function Nt(){x(k,k.current),x(Yl,Yl.current)}function Ml(l){cl(Yl),xl===l&&(xl=null),cl(k)}var k=Pl(0);function ce(l){for(var t=l;t!==null;){if(t.tag===13){var u=t.memoizedState;if(u!==null&&(u=u.dehydrated,u===null||Uc(u)||Hc(u)))return t}else if(t.tag===19&&(t.memoizedProps.revealOrder==="forwards"||t.memoizedProps.revealOrder==="backwards"||t.memoizedProps.revealOrder==="unstable_legacy-backwards"||t.memoizedProps.revealOrder==="together")){if((t.flags&128)!==0)return t}else if(t.child!==null){t.child.return=t,t=t.child;continue}if(t===l)break;for(;t.sibling===null;){if(t.return===null||t.return===l)return null;t=t.return}t.sibling.return=t.return,t=t.sibling}return null}var ot=0,M=null,j=null,P=null,ie=!1,Lu=!1,vu=!1,ye=0,Ja=0,Ku=null,dh=0;function $(){throw Error(b(321))}function li(l,t){if(t===null)return!1;for(var u=0;u<t.length&&u<l.length;u++)if(!Bl(l[u],t[u]))return!1;return!0}function ti(l,t,u,a,n,e){return ot=e,M=t,t.memoizedState=null,t.updateQueue=null,t.lanes=0,O.H=l===null||l.memoizedState===null?nv:di,vu=!1,e=u(a,n),vu=!1,Lu&&(e=Ny(t,u,a,n)),Hy(l),e}function Hy(l){O.H=ra;var t=j!==null&&j.next!==null;if(ot=0,P=j=M=null,ie=!1,Ja=0,Ku=null,t)throw Error(b(300));l===null||ul||(l=l.dependencies,l!==null&&ne(l)&&(ul=!0))}function Ny(l,t,u,a){M=l;var n=0;do{if(Lu&&(Ku=null),Ja=0,Lu=!1,25<=n)throw Error(b(301));if(n+=1,P=j=null,l.updateQueue!=null){var e=l.updateQueue;e.lastEffect=null,e.events=null,e.stores=null,e.memoCache!=null&&(e.memoCache.index=0)}O.H=ev,e=t(u,a)}while(Lu);return e}function hh(){var l=O.H,t=l.useState()[0];return t=typeof t.then=="function"?en(t):t,l=l.useState()[0],(j!==null?j.memoizedState:null)!==l&&(M.flags|=1024),t}function ui(){var l=ye!==0;return ye=0,l}function ai(l,t,u){t.updateQueue=l.updateQueue,t.flags&=-2053,l.lanes&=~u}function ni(l){if(ie){for(l=l.memoizedState;l!==null;){var t=l.queue;t!==null&&(t.pending=null),l=l.next}ie=!1}ot=0,P=j=M=null,Lu=!1,Ja=ye=0,Ku=null}function ol(){var l={memoizedState:null,baseState:null,baseQueue:null,queue:null,next:null};return P===null?M.memoizedState=P=l:P=P.next=l,P}function I(){if(j===null){var l=M.alternate;l=l!==null?l.memoizedState:null}else l=j.next;var t=P===null?M.memoizedState:P.next;if(t!==null)P=t,j=l;else{if(l===null)throw M.alternate===null?Error(b(467)):Error(b(310));j=l,l={memoizedState:j.memoizedState,baseState:j.baseState,baseQueue:j.baseQueue,queue:j.queue,next:null},P===null?M.memoizedState=P=l:P=P.next=l}return P}function Be(){return{lastEffect:null,events:null,stores:null,memoCache:null}}function en(l){var t=Ja;return Ja+=1,Ku===null&&(Ku=[]),l=Ay(Ku,l,t),t=M,(P===null?t.memoizedState:P.next)===null&&(t=t.alternate,O.H=t===null||t.memoizedState===null?nv:di),l}function Ye(l){if(l!==null&&typeof l=="object"){if(typeof l.then=="function")return en(l);if(l.$$typeof===yt)return ml(l)}throw Error(b(438,String(l)))}function ei(l){var t=null,u=M.updateQueue;if(u!==null&&(t=u.memoCache),t==null){var a=M.alternate;a!==null&&(a=a.updateQueue,a!==null&&(a=a.memoCache,a!=null&&(t={data:a.data.map(function(n){return n.slice()}),index:0})))}if(t==null&&(t={data:[],index:0}),u===null&&(u=Be(),M.updateQueue=u),u.memoCache=t,u=t.data[t.index],u===void 0)for(u=t.data[t.index]=Array(l),a=0;a<l;a++)u[a]=Im;return t.index++,u}function st(l,t){return typeof t=="function"?t(l):t}function Vn(l){var t=I();return fi(t,j,l)}function fi(l,t,u){var a=l.queue;if(a===null)throw Error(b(311));a.lastRenderedReducer=u;var n=l.baseQueue,e=a.pending;if(e!==null){if(n!==null){var f=n.next;n.next=e.next,e.next=f}t.baseQueue=n=e,a.pending=null}if(e=l.baseState,n===null)l.memoizedState=e;else{t=n.next;var c=f=null,i=null,m=t,g=!1;do{var s=m.lane&-536870913;if(s!==m.lane?(p&s)===s:(ot&s)===s){var h=m.revertLane;if(h===0)i!==null&&(i=i.next={lane:0,revertLane:0,gesture:null,action:m.action,hasEagerState:m.hasEagerState,eagerState:m.eagerState,next:null}),s===Wu&&(g=!0);else if((ot&h)===h){m=m.next,h===Wu&&(g=!0);continue}else s={lane:0,revertLane:m.revertLane,gesture:null,action:m.action,hasEagerState:m.hasEagerState,eagerState:m.eagerState,next:null},i===null?(c=i=s,f=e):i=i.next=s,M.lanes|=h,Wt|=h;s=m.action,vu&&u(e,s),e=m.hasEagerState?m.eagerState:u(e,s)}else h={lane:s,revertLane:m.revertLane,gesture:m.gesture,action:m.action,hasEagerState:m.hasEagerState,eagerState:m.eagerState,next:null},i===null?(c=i=h,f=e):i=i.next=h,M.lanes|=s,Wt|=s;m=m.next}while(m!==null&&m!==t);if(i===null?f=e:i.next=c,!Bl(e,l.memoizedState)&&(ul=!0,g&&(u=Vu,u!==null)))throw u;l.memoized
