## index.json 接口

index.json 类型为 TemplateInfo[]

```typescript

export type TemplateCategory =
    '8051' | 'STM8' | 'PIC' | 'STM32' | 'MM32' | 'GD32' | 'NXP' | // vendor type
    'FreeRTOS' | 'uCOS-II' | 'RT-Thread-Nano' | // OS type

export interface TemplateInfo {

    file_name: string;

    display_name: string;

    category: TemplateCategory[];

    version: string;
    
    author: string | undefined;

    download_url: string | undefined;

    size: number | undefined;

    disabled: boolean | undefined;

    upload_time: string | undefined;

    update_time: string | undefined;
}

```
