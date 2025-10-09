# 💬 CorralX Echo Server

**Servidor WebSocket para chat en tiempo real**

Laravel Echo Server configurado para CorralX, permitiendo mensajería instantánea entre compradores y vendedores.

---

## 🚀 Inicio Rápido

```bash
# Instalar dependencias
npm install

# Iniciar servidor en modo desarrollo
npm run start:dev

# O usar el script de inicio
./start.sh
```

---

## ⚙️ Configuración

### **Endpoints:**
- **WebSocket**: `ws://192.168.27.12:6001`
- **Auth Backend**: `http://192.168.27.12:8000`
- **Auth Endpoint**: `/broadcasting/auth`

### **Clientes:**
- **App ID**: `corralx-app`
- **Key**: `corralx-secret-key-2025`

---

## 📡 Canales Disponibles

### **Canal Privado: `conversation.{id}`**
- Mensajes 1:1 entre usuarios
- Autenticación requerida
- Solo participantes de la conversación pueden escuchar

### **Eventos:**
- `MessageSent` - Nuevo mensaje en conversación
- `TypingStarted` - Usuario comenzó a escribir
- `TypingStopped` - Usuario dejó de escribir
- `MessageRead` - Mensaje marcado como leído

---

## 🔒 Seguridad

- ✅ Autenticación vía Laravel Sanctum
- ✅ Canales privados por conversación
- ✅ Verificación de participantes
- ✅ CORS configurado

---

## 📊 Monitoring

Ver logs en tiempo real:
```bash
tail -f echo-server.log
```

---

## 🐛 Troubleshooting

### Error: "Connection refused"
- Verificar que el backend esté corriendo en puerto 8000
- Verificar IP en `laravel-echo-server.json`

### Error: "Unauthorized"
- Verificar que broadcasting esté habilitado en backend
- Verificar token de autenticación en requests

---

**Estado:** ✅ Configurado y listo para CorralX  
**Versión:** 1.0.0  
**Laravel Echo Server:** v1.6.3
