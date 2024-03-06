## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

For me

CSS Style
    - We can declare global css such as theme colors, font on global.css and import it on import zone on file
    - We can create class of css and then import and use it as a object as home.module.css and we i use it on page.tsx
    - 'clsx' it is lib that use to conditional toggle css style or classname
    - on tailwind css if we use class like this classname="hidden md:block" => it mean on device is medium or larger breakpoint it will be show block but when screen is less than md that will be hidden

Font and Images
    - next/font it will download font on building that mean it will be static font
    - next/image we should to set width and height to avoid shift on different screen 

Layouts and Pages
    - next.js already includes nest routing by it will be binding with folder project
    - we can use page.tsx to declare it will be page and route such as
        - / => /app/page.tsx
        - /dashboard => /app/dashboard/page.tsx 
        - /dashboard/invoice => /app/dashboard/invoice/page.tsx 
    - when we use layout we must to pass children as props to render children can be page or another layout
    - from example layout will wrap all page on dashboard route so children will render only page and nest page on dashboard
    - while it will navigate route only component will be update but layout doesn't re-render that we call partial rendering

Link
    - <a/> and <Link/> use to navigate page but it different <a/> it will be server side navigate so it will full page refresh but <Link/> it is client side navigate so it will not full page refresh because <Link/> will be prefetch code for linking route
    - We cab do active link on rendering by use usePathname that be Client Component. 
    - If we want to use client component we must to declare "use client" on top of file