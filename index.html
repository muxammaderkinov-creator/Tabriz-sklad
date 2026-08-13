-- ==========================================
-- Программа: Tabriz sklad
-- Разработано для: MUSTAFAYEV ACADEMY
-- Назначение: Учёт склада мебельной структуры
-- ==========================================

-- 1. ТАБЛИЦА: Категории мебели (Шкафы, Столы, Фурнитура, ЛДСП и т.д.)
CREATE TABLE categories (
    category_id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    description TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- 2. ТАБЛИЦА: Товары (Мебельная структура, Фото, Горячие продажи, Цена)
CREATE TABLE products (
    product_id SERIAL PRIMARY KEY,
    category_id INT REFERENCES categories(category_id) ON DELETE SET NULL,
    sku VARCHAR(50) UNIQUE NOT NULL,            -- Артикул / Штрихкод
    name VARCHAR(150) NOT NULL,                 -- Наименование товара/детали
    material VARCHAR(100),                      -- Материал (например, ЛДСП 18мм, МДФ)
    dimensions VARCHAR(50),                     -- Габариты (ШхВхГ)
    purchase_price DECIMAL(12, 2) NOT NULL,     -- Себестоимость (закупка)
    sale_price DECIMAL(12, 2) NOT NULL,         -- Цена продажи
    stock_quantity INT DEFAULT 0,               -- Текущий остаток на складе
    min_stock_level INT DEFAULT 2,              -- Минимальный остаток для уведомлений
    photo_url TEXT,                             -- Ссылка/путь к фото товара
    is_hot_sale BOOLEAN DEFAULT FALSE,          -- Флаг "Горячие продажи" (Быстрая кнопка)
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- 3. ТАБЛИЦА: Клиентская база
CREATE TABLE clients (
    client_id SERIAL PRIMARY KEY,
    full_name VARCHAR(150) NOT NULL,
    phone VARCHAR(30) UNIQUE NOT NULL,
    email VARCHAR(100),
    address TEXT,                               -- Адрес доставки мебели
    discount_percent DECIMAL(5, 2) DEFAULT 0.00, -- Персональная скидка (%)
    notes TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- 4. ТАБЛИЦА: Шапка продаж (Заказы / Чек)
CREATE TABLE sales (
    sale_id SERIAL PRIMARY KEY,
    client_id INT REFERENCES clients(client_id) ON DELETE SET NULL,
    sale_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    total_amount DECIMAL(12, 2) NOT NULL DEFAULT 0.00,
    payment_method VARCHAR(50) DEFAULT 'Cash',  -- Наличные, Карта, Перевод
    status VARCHAR(30) DEFAULT 'Completed'      -- Завершен, В обработке, Отменен
);

-- 5. ТАБЛИЦА: Позиции в чеке (Детализация продаж)
CREATE TABLE sale_items (
    sale_item_id SERIAL PRIMARY KEY,
    sale_id INT REFERENCES sales(sale_id) ON DELETE CASCADE,
    product_id INT REFERENCES products(product_id),
    quantity INT NOT NULL CHECK (quantity > 0),
    unit_price DECIMAL(12, 2) NOT NULL,         -- Фиксация цены на момент продажи
    subtotal DECIMAL(12, 2) NOT NULL
);

-- 6. ТАБЛИЦА: Движение товаров (Приход / Списание / Возврат)
CREATE TABLE inventory_transactions (
    transaction_id SERIAL PRIMARY KEY,
    product_id INT REFERENCES products(product_id) ON DELETE CASCADE,
    transaction_type VARCHAR(20) CHECK (transaction_type IN ('IN', 'OUT', 'ADJUSTMENT')),
    quantity INT NOT NULL,
    note TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
