# $NetBSD: Makefile,v 1.3 2017/12/06 21:48:40 jdolecek Exp $

MODNAME=		sodium
CATEGORIES+=		security
COMMENT=		PHP extension for the sodium crypto algorithms library

CONFIGURE_ARGS+=	--with-${MODNAME}=${BUILDLINK_PREFIX.libsodium}

PHP_VERSIONS_ACCEPTED=	72

.include "../../lang/php/ext.mk"
.include "../../security/libsodium/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
