# next config тохиргоонууд

#### Public зураг тохируулах

<figure><img src="../.gitbook/assets/Screenshot 2025-01-20 at 11.49.44 AM.png" alt=""><figcaption></figcaption></figure>

Ийм алдаа гарсан уу? Дараах тохиргоор **next.config.ts-**&#x442; оруулаарай.&#x20;

```
import type { NextConfig } from 'next';

const nextConfig: NextConfig = {
  images: {
    remotePatterns: [
      {
        protocol: 'https',
        hostname: '**',
      },
    ],
  },
};

```



